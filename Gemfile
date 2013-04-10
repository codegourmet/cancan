source "http://rubygems.org"


case ENV["MODEL_ADAPTER"]
when "active_record"
  gem "sqlite3"
  gem "activerecord", '~> 3.0.9', :require => "active_record"
  gem "with_model", '~> 0.1.5'
  gem "meta_where"
when "data_mapper"
  gem "dm-core", "~> 1.0.2"
  gem "dm-sqlite-adapter", "~> 1.0.2"
  gem "dm-migrations", "~> 1.0.2"
when "mongoid"
  gem "bson_ext", "~> 1.1"
  gem "mongoid", "~> 2.0.0.beta.20"
when nil, "mongo_mapper"
  gem "bson_ext"
  gem "mongo_mapper"
else
  raise "Unknown model adapter: #{ENV["MODEL_ADAPTER"]}"
end

gemspec
