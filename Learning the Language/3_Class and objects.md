          class person(object):
              def __init__(self,name,age,wt):
                  self.name = name
                  self.age = age
                  self.wt = wt

              def speak(self):
                  print("Hi, I am " + self.name + " and my age is :",self.age)

              def check(self):
                  if self.wt>100:
                      print("Fat ass!")
                  else:
                      print("Okay")

              def addAge(self,newAge):
                  self.age = self.age + newAge

              def wallet(self,money):
                  self.money = money

              def balance(self):
                  print("Balance : $", self.money)

              def addMoney(self,newMoney):
                  self.money += newMoney


          ms = person('fred',20,120)
          ms.speak()
          ms.check()
          ms.addAge(20)
          ms.speak()
          ms.wallet(456000)
          ms.balance()
          ms.addMoney(4000)
          ms.balance()

          #########Inheritance#############

          class Indian(person):
              def __init__(self,name,age,wt,color):
                  super().__init__(name,age,wt)
                  self.color = color

              def speak(self):
                  print("Hi, I am " + self.name + " and my age is :",self.age," and my coplexion is : ",self.color)

              def wallet(self,money):
                  self.money = money/74

              def addMoney(self,newMoney):
                  self.money += (newMoney/74)

              def religion(self,belief):
                  if(belief==1):
                      print('You believe in God!')
                  else:
                      print('You are an athiest!')


          ind = Indian('Sadhguru',75,85,'brown')
          ind.speak()
          ind.check()
          ind.wallet(740000)
          ind.balance()
          ind.addMoney(74000)
          ind.balance()
          ind.religion(1)




