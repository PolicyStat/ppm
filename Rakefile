## -- Misc Configs -- ##

public_dir      = "public"    # compiled site directory
server_port     = "4000"      # port for preview server eg. localhost:4000

desc "preview the site in a web browser"
task :preview do
  puts "Starting Rack on port #{server_port}"
  rackupPid = spawn("rackup --port #{server_port}")

  trap("INT") {
	Process.kill(9, rackupPid)
	exit 0
  }

  Process.wait
end
