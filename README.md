```
10041  cd rubyspace
10042  cd toy_app
10043  bundle install
10044  rails s
10045  rails generate scaffold User name:string email:string
10046  rake db:migrate
10047  rails generate scaffold Micropost content:text user_id:integer
10048  rake db:migrate
10049  atom .
10050  rails s
```
```
10051  git init
10052  git add .
10054  git commit -m "initial commit"
```

```
10055  heroku create
10056  git push heroku master
10057  bundle install
10058  git add .
10059  git commit -m "update gimfile gem pg"
10060  git push heroku master
10061  heroku run rake db:migrate
10062  heroku open
```
```
class User < ApplicationRecord
  has_many :microposts
  validates :name, presence: true
  validates :email, presence: true
end
```
```
class Micropost < ApplicationRecord
  belongs_to :user
  validates :content, length: { maximum: 140 }, presence: true
end
```


```
group :development, :test do
  gem 'sqlite3'
  # Call 'byebug' anywhere in the code to stop execution and get a debugger console
  gem 'byebug', platforms: [:mri, :mingw, :x64_mingw]
end

group :production do
  gem 'pg', '0.18.4'
end
```
