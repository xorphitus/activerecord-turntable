# A sample Guardfile
# More info at https://github.com/guard/guard#readme

guard "rspec",
      cmd: "bundle exec rspec",
      all_after_pass: true,
      all_on_start: true do
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^lib/(.+)\.rb$})     { |m| "spec/#{m[1]}_spec.rb" }
  watch("spec/spec_helper.rb")  { "spec" }
end

guard :rubocop do
  watch(/.+\.rb$/)
  watch(%r{(?:.+/)?\.rubocop\.yml$}) { |m| File.dirname(m[0]) }
end
