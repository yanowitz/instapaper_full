# instapaper_full

Ruby wrapper for the [Instapaper Full API](http://www.instapaper.com/api/full)

Draft version.

Note that you need to [request OAuth Application tokens manually](http://www.instapaper.com/main/request_oauth_consumer_token) and that most methods only work for Instapaper subscribers.

# Installation

    gem install instapaper_full

# Examples

    ip = InstapaperFull::API.new :consumer_key => "my key", :consumer_secret => "my secret"
    ip.authenticate "someone@example.com", "password"
    puts ip.options.user_id
    puts ip.bookmarks_list(:limit => 1)[0]['url']
