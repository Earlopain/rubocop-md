# Before All

Rails has a great feature – `transactional_tests`, i.e. running each example within a transaction which is roll-backed in the end.

Of course, we can do something like this:

```ruby
describe BeatleWeightedSearchQuery do
  before(:each) do
    @paul = create(:beatle, name: "Paul")
    @ringo = create(:beatle, name: "Ringo")
    @george = create(:beatle, name: "George")
    @john = create(:beatle, name: 'John')
  end

  # Lint/UnusedMethodArgument. The plugin config excludes this,
  # verify that user configs with cop excludes inherit that
  def do_something(foo)
    puts "FOO"
  end

  # and about 15 examples here
end
```
