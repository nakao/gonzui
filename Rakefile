require 'rubygems'
gem 'hoe', '>= 2.1.0'
require 'hoe'
require 'fileutils'
require './lib/gonzui'

Hoe.plugin :newgem
# Hoe.plugin :website
# Hoe.plugin :cucumberfeatures

# Generate all the Rake tasks
# Run 'rake -T' to see list of generated tasks (from gem root directory)
$hoe = Hoe.spec 'gonzui' do
  self.developer 'mallowlabs', 'mallowlabs@gmail.com'
  self.post_install_message = File.read('PostInstall.txt')
  self.rubyforge_name       = self.name # TODO this is default value
  self.extra_deps         = [['langscan','>= 1.2']] #['bdb', '>= 0.5.2']

end

require 'newgem/tasks'
Dir['tasks/**/*.rake'].each { |t| load t }

# TODO - want other tests/tasks run by default? Add them to the list
# remove_task :default
# task :default => [:spec, :features]


