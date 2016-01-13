desc "Serve jekyll blog"
task :serve do
   puts "\n## Building archives"
   status = system("ruby archive/_generator.ruby")
   puts status ? "Success" : "Failed"
   puts "\n## Starting local server with --watch option"
   status = system("jekyll serve -H $IP -P $PORT --watch");
   puts status ? "Success" : "Failed"
end

desc "Build _site/"
task :build do 
  puts "\n## Purging _site directory"
  status = system("find ./_site/* -maxdepth 1 ! -name 'archive' ! -name '.git' ! -name '.*' | xargs rm -rf")
  puts status ? "Success" : "Failed"
  puts "\n## Building the website underneath _site directory"
  status = system("jekyll build")
  puts status ? "Success" : "Failed"
  puts "\n## Building archives"
  status = system("ruby archive/_generator.ruby")
  puts status ? "Success" : "Failed" 
end  

desc "Deploy _site/"
task :deploy do
  message = "Committing at #{Time.now.utc}"
  puts "\n## Checking in Source"
  status = system("git add -A; git commit -m \"#{message}\"; git push -u origin source")
  puts status ? "Success" : "Failed"
  puts "\n## Checking in Master (site)"
  status = system("cd ./_site/; git add -A; git commit -m \"#{message}\"; git push -u origin master")
  puts status ? "Success" : "Failed"
end

desc "Build, deploy, serve"
task :all => [:build, :deploy] do
end
