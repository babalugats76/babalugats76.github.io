desc "Serve jekyll blog"
task :serve do
   puts "\n## Building archives"
   status = system("ruby archive/_generator.ruby")
   puts status ? "Success" : "Failed"
   puts "\n## Starting local server with --watch option"
   status = system("jekyll serve -H $IP -P $PORT --watch");
   puts status ? "Success" : "Failed"
end

desc "CD test"
task :cd do 
   system("cd _site; ls -l;")
end

desc "Build _site/"
task :build do 
  puts "\n## Purging _site directory"
  status = system("find ./_site/* -maxdepth 1 ! -name '.git' ! -name '.*' | xargs rm -rf")
  puts status ? "Success" : "Failed"
  puts "\n## Building the website"
  status = system("jekyll build")
  puts status ? "Success" : "Failed"
  puts "\n## Building archives"
  status = system("ruby archive/_generator.ruby")
  puts status ? "Success" : "Failed" 
end  

desc "Deploy _site/"
task :deploy do
  puts "\n## Staging source files"
  status = system("git add -A")
  puts status ? "Success" : "Failed"
  puts "\n## Committing source"
  message = "Committing at #{Time.now.utc}"
  status = system("git commit -m \"#{message}\"")
  puts status ? "Success" : "Failed"
  puts "\n## Pushing commits to source branch"
  status = system("git push -u origin source")
  puts status ? "Success" : "Failed"
  puts "\n## Committing master"
  puts "\n## Staging master (site) files"
  puts "Changing directory to _site"
  system("cd ./_site/");
  status = system("git add -A")
  puts status ? "Success" : "Failed"
  message = "Committing master at #{Time.now.utc}"
  status = system("git commit -m \"#{message}\"")
  puts status ? "Success" : "Failed"
  puts "\n## Pushing commits to source branch"
  status = system("git push -u origin master")
  puts status ? "Success" : "Failed"
  puts "Changing directory back to ."
  system("cd ..");
end

desc "Build, deploy, serve"
task :all => [:build, :deploy] do
end
