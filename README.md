### classifier-reborn
---

https://github.com/jekyll/classifier-reborn

https://www.classifier-reborn.com/

```
gem install classifier-reborn
irb
require 'classifier-reborn'
classifier = ClassifierReborn::Bayes.new '', ''
classifier.train "", ""
classifier.train "", ""
classifier.classify ""
# => "Ham"
lsi = ClassifierReborn::LSI.new
lsi.add_item "", :dog
lsi.add_item "", :dog
lsi.add_item "", :cat
lsi.add_item "", :cat
lsi.add_item "", :bird
lsi.classify ""
# => :dog
# => [""]

gem 'classifier-reborn-jruby', platforms: :java
```

```
git clone git@github.com:jekyll/classifier-reborn.git
cd classifier-reborn
bundle install
gem install redis
rake

redis-server --demonize yes
rake
rake bench
rake validate

git clone git@github.com:jekyll/classidier-reborn.git
cd classifier-reborn
docker build -t classifier-reborn .

docker run --rm -it -v "$PWD":/usr/src/app classidier-reborn

pry >
require 'classifier-reborn'
classifier = ClassifierReborn::Bayes.new '', ''

docker run --rm -it -v "$PWD":/usr/src/app -w /usr/src/app/docs -p 4000:4000 classifier-reborn jekyll s -H 0.0.0.0

```

```

```


