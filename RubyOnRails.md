```rails
rails generate model Category

```

```ruby
class CreateCategories < ActiveRecord::Migration
  def change
    create_table :categories do |t|
			t.string :name
			t.string :thumburl
      t.timestamps
    end
  end
end
```

```rails
rake db:migrate
```

```rails
rails generate controller Persons index new edit
```

```ruby
  def category_params
  	params.require(:category).permit(:name, :thumburl)
  end
```

