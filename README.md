
class Examinee
  @@test_taker = []
  attr_reader :name,:score
  def initialize(name,score)
    @name = name
    @score = score
  end

  def storage(i)
    @@test_taker << i
  end

  def max
    max = @@test_taker.max_by { |human| human.score }
    p "最高得点は#{max.score}です。"
    p "最高得点者は#{max.name}です。"
  end

  def average
    average = []
    @@test_taker.each { |human| average << human.score }
    p "平均点は#{ average.sum(0.0) / average.size }点です。"
  end

end

e = { アイダ: 80 ,イウダ: 80, ウエダ: 40, エオダ: 60}
m = { アイダ: 60 ,イウダ: 80, ウエダ: 90, エオダ: 70}

man = nil
e.each do |name,score|
  man = Examinee.new(name,score)
  man.storage(man)
end

# 最高点を出す 得点者を出す
man.max
#平均値を出す
man.average
