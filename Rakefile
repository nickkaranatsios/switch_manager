task :default => :cucumber # rubocop:disable HashSyntax
task :travis => :cucumber # rubocop:disable HashSyntax

begin
  require 'cucumber/rake/task'
  Cucumber::Rake::Task.new do |t|
    t.cucumber_opts = '--tags ~@wip'
  end
rescue LoadError
  task :cucumber do
    $stderr.puts 'Cucumber is disabled'
  end
end
