require "capistrano/setup"
require "capistrano/deploy"
require 'capistrano/rails'
require 'capistrano/rvm'
require 'capistrano/puma'
require "capistrano/scm/git"

set :rbenv_type, :user
set :rbenv_ruby, '2.5.0'

install_plugin Capistrano::SCM::Git
install_plugin Capistrano::Puma
install_plugin Capistrano::Puma::Workers
install_plugin Capistrano::Puma::Nginx

Dir.glob("lib/capistrano/tasks/*.rake").each { |r| import r }
