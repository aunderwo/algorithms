require 'rubygems'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "algorithms-aunderwo"
    gemspec.summary = "A library of algorithms and containers."
    gemspec.description = "A modfication of the algorithms gem to include the latest String function"
    gemspec.email = "algorithms@ants.otherinbox.co, kanwei@gmail.com"
    gemspec.homepage = "http://github.com/aunderwo/algorithms"
    gemspec.authors = ["Kanwei Li", "Anthony Underwood"]
  end
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end


task :push do
  sh "git push"    # Rubyforge
  sh "git push --tags"    # Rubyforge
  sh "git push gh" # Github
  sh "git push gh --tags" # Github
end

task :hanna do
  sh "rm -fr doc"
  sh "hanna -SN lib/ -m Algorithms"
  sh "scp -rq doc/* kanwei@rubyforge.org:/var/www/gforge-projects/algorithms"
end

