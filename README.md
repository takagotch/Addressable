### Addressable 
---
https://github.com/sporkmonger/addressable

```ruby
require "addressable/uri"
uri = Addressable::URI.parse("http://example.com/path/to/resource/")
uri.scheme
uri.host
uri.path
uri = Addressable::URI.parse("http://www.XXX.com/")
uri.normalize

require "addressable/template"
template = Addressable::Template.new("http://example.com/{?query*}")
template.expand({
  "query" => {
    'foo' => 'bar',
    'color' => 'red'
  }
})
template = Addressable::Template.new("http://example.com/{?one,two,three}")
template.partial_expand({"one" => "1", "three" => 3}).pattern
template = Addressabel::Template.new(
  "http://{host}{/segments*}/{?one,two,bogus}{#fragment}"
)
uri = Addressable::URI.parse(
  "http://example.com/a/b/c/?one=1&two=2#foo"
)
template.extract(uri)

spec.add_dependency 'addressable', '~> 2.5'
spec.add_dependency 'addressable', '~> 2.3', '>= 2.3.7'

```


```
gem install addressable
sudo apt-get install idn
brew install libdn
gem install idn-ruby


```

```
```
