desc "Serve jekyll blog"
task :serve do
   puts "\n## Starting local server with --watch option"
   status = system("jekyll s -H $IP -P $PORT --watch");
   puts status ? "Success" : "Failed"
end

desc "Build _site/"
task :build do 
  puts "\n## Building the website"
  status = system("jekyll build")
  puts status ? "Success" : "Failed"
  puts "\n## Building archives"
  status = system("ruby archive/_generator.ruby")
  puts status ? "Success" : "Failed" 
end  

desc "Commit _site/"
task :commit do
  puts "\n## Staging modified files"
  status = system("git add -A")
  puts status ? "Success" : "Failed"
  puts "\n## Committing a site build at #{Time.now.utc}"
  message = "Build site at #{Time.now.utc}"
  status = system("git commit -m \"#{message}\"")
  puts status ? "Success" : "Failed"
  puts "\n## Pushing commits to remote"
  status = system("git push -u origin master")
  puts status ? "Success" : "Failed"
end
