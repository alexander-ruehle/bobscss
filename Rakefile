require 'rubygems'
require 'rake'

# gem install sass

desc 'Compile CSS'
namespace :compile do
  # task is only used in development
  task :development do
    compile_components
  end

  # task is only used when generating new releases
  task :production do
    compile_components
    gzip_components
  end

  # compiles framework into one file and minimized files
  def compile_components
    # standard flexbox
    system 'sass scss/bobscss.scss:bobscss.css --style expanded'
    system 'sass scss/bobscss.scss:bobscss.min.css --style compressed'

    # flexless grid
    system 'sass scss/bobscss-flexless.scss:bobscss-flexless.css --style expanded'
    system 'sass scss/bobscss-flexless.scss:bobscss-flexless.min.css --style compressed'
  end

  # gzips compiled and minimized framework
  # @hint: can only be used after :compile_components
  def gzip_components
    system 'gzip -c bobscss.min.css > bobscss.min.css.gz'
    system 'gzip -c bobscss-flexless.min.css > bobscss-flexless.min.css.gz'
  end
end