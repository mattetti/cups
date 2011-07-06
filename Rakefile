# use https://github.com/luislavena/rake-compiler
require 'rake/extensiontask'

spec = Gem::Specification.new do |s|
  s.name = %q{cups}
  s.version = "0.0.8"
  s.authors = ["Ivan Turkovic", "Chris Mowforth", "Matt Aimonetti"]
  s.email = ["me@ivanturkovic.com", "chris@mowforth.com"]
  s.summary = "A lightweight Ruby library for printing."
  s.platform = Gem::Platform::RUBY
  s.description = <<-EOF
    Ruby CUPS provides a wrapper for the Common UNIX Printing System, allowing rubyists to perform basic tasks like printer discovery, job submission & querying.
  EOF
  s.files = Dir.glob("{lib}/**/*")
  s.extensions = FileList["ext/**/extconf.rb"]
  s.homepage = "https://github.com/mattetti/cups"
  s.has_rdoc = true
  s.rubyforge_project = "mattetti_cups"
end

# add your default gem packing task
Gem::PackageTask.new(spec) do |pkg|
end

# feed the ExtensionTask with your spec
Rake::ExtensionTask.new('cups', spec)
