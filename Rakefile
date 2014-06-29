require 'rubygems'
require 'rake'

desc 'Compile CSS'
task :compile do
  system 'sass scss/bobscss.scss:bobscss.css --style expanded'
  system 'sass scss/bobscss.scss:bobscss.min.css --style compressed'
  system 'gzip -c bobscss.min.css > bobscss.min.css.gz'
end
