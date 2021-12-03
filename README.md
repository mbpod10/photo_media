### Photo Media
```
$ rails _6.1.4.1_ new photo_app
$ rails generate controller welcome index  
```

```rb
# GEMFILE
gem 'devise'
gem 'twitter-bootstrap-rails'
gem 'devise-bootstrap-views'
```

```
$ rails generate devise:install
$ rails generate devise User
```


```rb
# db/migrate/MIGRATION_devise_create_users.rb
t.string   :confirmation_token
t.datetime :confirmed_at
t.datetime :confirmation_sent_at
t.string   :unconfirmed_email 
```

#### Include Confirmables
```rb
class User < ApplicationRecord
  # Include default devise modules. Others available are:
  # :confirmable, :lockable, :timeoutable, :trackable and :omniauthable
  devise :database_authenticatable, :registerable, :confirmable, <===
         :recoverable, :rememberable, :validatable
end
```

#### Styling
```
$ rails generate bootstrap:install static
$ rails generate bootstrap:layout application
$ rails generate devise:views:locale en
$ rails generate devise:views:bootstrap_templates
```
