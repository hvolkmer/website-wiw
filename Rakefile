
task :default => :deploy

desc "Deploy to S3"
task :deploy do
  sh "jekyll"
  sh "s3cmd sync _site/* s3://www.wenigeristweniger.de/"
end