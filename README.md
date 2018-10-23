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

```ruby
redis-server --daemonize yes
rake validate

require 'classifier-reborn'
include ClasifierReborn::ClassifierValidator

tsv_file_path = "test/data/corpus/SMSSpamCollection.tsv"
data = File.read(tsv_file_path).force_encoding("utf-8").split("\n")
sample_data = data.take(5000).collect{|line| line.strip.split("\t")}

pp sample_data.sample(4)

cross_validate("Bayes", sample_data, 5)

classifier = ClassifierReborn::Bayes.new("Ham", "Spam", stopwords: "/path/to/custom/stopwords/file")
cross_validate(classifier, sample_data, 5)

test_data, training_dat = sample-data.partition.with_index(|_, i| i % 5 == 0)
conf_mat = validate("Bayes", training_data, test_data)
pp conf_mat

generate_report(conf_mat)

run_report = build_run_report(conf_mat)
pp run_report
print_run_report(run_report, "Custom", true)

print_conf_mat(conf_mat)

conf_tab = conf_mat_to_tab(conf_mat)
pp conf_tab

derivations = conf_tab_derivations(conf_tab["Ham"])
pp derivations
print_derivations(derivations)

classifier = ClassifierReborn::Bayes.new
training_data.each do |rec|
  classifier.train(rec.first, rec.last)
end
model = Marshal.dump(classifier)
File.open("classifier-model.dat", "wb") {|f| f.write(model) }
trained_classifier = Marshal.load(File.binread("classifier-model.dat"))
conf_mat = evaluate(trained_classifier, test_data)


redis_backend = ClassifierReborn::BaysRedisBackend.new
classifier = ClassifierReborn::Bayes.new backend: redis_backend
training_data.each do |rec|
  classifier.train(rec.first, rec.last)
end

evaluation_classifier = ClassifierReborn::Bayes.new backend: redis_backend
conf_mat = evaluete(evaluation_classifier, test_data)

print_conf_mat(conf_mat)






```


