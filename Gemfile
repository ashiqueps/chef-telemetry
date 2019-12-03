source "https://rubygems.org"

# Specify your gem's dependencies in chef-telemetry.gemspec
gemspec

group :debug do
  gem "pry"
  gem "pry-byebug"
  gem "pry-stack_explorer"
end

group :test do
  gem "chefstyle", "= 0.10.0"
  gem "rake"
  gem "rspec", "~> 3.0"
end

group :docs do
  gem "github-markup"
  gem "redcarpet"
  gem "yard"
end

instance_eval(ENV["GEMFILE_MOD"]) if ENV["GEMFILE_MOD"]

# If you want to load debugging tools into the bundle exec sandbox,
# add these additional dependencies into Gemfile.local
eval_gemfile("Gemfile.local") if File.exist?("Gemfile.local")
