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
