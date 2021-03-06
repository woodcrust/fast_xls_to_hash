## FastXlsToHash

[![Code Climate](https://codeclimate.com/github/woodcrust/fast_xls_to_hash/badges/gpa.svg)](https://codeclimate.com/github/woodcrust/fast_xls_to_hash)

This gem can to convert your xls to hash ! Really cool ! It's amazing gem, it's true.

```ruby
example: { :list_1 => 
             { :row_1 => 
               { :column_1 => 'value',
                 :column_2 => 100,
                 :column_3 => #<DateTime: 2016-11-01T00:00:00+00:00>
               },
               :row_2 => 
               { :column_1 => 'value2',
                 :column_2 => 200,
                 :column_3 => #<DateTime: 2016-12-01T00:00:00+00:00>
               }
             },
           :list_2 => {...} 
         }
```
or if you want to use xls style of names

```ruby
FastXlsToHash.with_xls_style = true
```

```ruby
example: { :list_1 => 
             { :'1' => 
               { :A => 'value',
                 :B => 100,
                 :C => #<DateTime: 2016-11-01T00:00:00+00:00>
               },
               :'2' => 
               { :A => 'value2',
                 :B => 200,
                 :C => #<DateTime: 2016-12-01T00:00:00+00:00>
               }
             },
           :list_2 => {...} 
         }
```

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'fast_xls_to_hash'
```

And then execute:

    $ bundle

Install it yourself as:

    $ gem install fast_xls_to_hash

## Usage

e.g. in rails
```ruby
class Example

  include FastXlsToHash
  FastXlsToHash.with_xls_style = true          #optional, default false

  dir_of_xls  = '/data/test.xls'
  hash_of_xls = ParseXls.to_hash(dir_of_xls)

end
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

