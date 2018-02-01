# Генерація проекту
rails new test_app -O //Параметр -O вказує що даний проект повинен бути згенерений без бази дани
# Підключаєм бібліотеки(для цього використовується Gemfile в корінному каталозі)
gem 'mongoid'
gem 'haml-rails'
# Генерим файл конфігурацій для бази даних(він зберігається в папці config/mongoid.yml)
rails g mongoid:config
# Перетворюємо erb файли в haml для зручності верстки
rails haml:erb2haml
# Генеримо всі файли для post за допомогою scaffold
rails g scaffold post title description:text
