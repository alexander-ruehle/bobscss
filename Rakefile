require 'rubygems'
require 'rake'

# gem install sass

desc 'Compile CSS'
task :compile do
  # standard flexbox bobscss
  system 'sass scss/bobscss.scss:bobscss.css --style expanded'
  system 'sass scss/bobscss.scss:bobscss.min.css --style compressed'
  system 'gzip -c bobscss.min.css > bobscss.min.css.gz'

  # flexless grid bobscss
  system 'sass scss/bobscss-flexless.scss:bobscss-flexless.css --style expanded'
  system 'sass scss/bobscss-flexless.scss:bobscss-flexless.min.css --style compressed'
  system 'gzip -c bobscss-flexless.min.css > bobscss-flexless.min.css.gz'
end
