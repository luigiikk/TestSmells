## The Ugly Mirror


```ruby
require "test/unit"

User = Struct.new(:first_name, :last_name, :email) do
  def to_s
    "#{last_name}, #{first_name} <#{email}>"
  end
end

class UserTest < Test::Unit::TestCase
  def test_to_s_includes_name_and_email
    user = User.new("John", "Smith", "jsmith@example.com")
    assert_equal "#{user.last_name}, #{user.first_name} <#{user.email}>", user.to_s
  end
end