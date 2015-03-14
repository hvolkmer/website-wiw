require 'html/proofer'

task :default => :publish

desc "Deploy to S3"
task :publish => :test do
  sh "s3_website push"
end

task :build do
  sh "bundle exec jekyll build"
end

task :test => :build do
  HTML::Proofer.new("./_site").run
end