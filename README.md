# nilofarMohamadi
import turtle
import random
Score=0
s=turtle.Screen()
s.setup(600,600)
s.title('likkkiiii')
s.bgcolor('lightgreen')
##1
wall=turtle.Turtle()
wall.up()
wall.goto(-275,275)
wall.down()
wall.width(4)
for i in range(4):
    wall.fd(550)
    wall.rt(90)
wall.ht()
##2
laki=turtle.Turtle()
laki.shape('turtle')
laki.color('darkgreen')
laki.shapesize(2)
laki.up()
###10
ball=turtle.Turtle()
ball.shape('circle')
ball.color('red')
ball.up()
ball.goto(random.randint(-260,260), random.randint(-260,260))
####2
wr=turtle.Turtle()
wr.up()
wr.goto(-270,275)
wr.ht()
wr.color('navy')
wr.write('امتیاز ='+ str(Score), font=('b koodak', 12,'bold'))
####20
def move_right():
  #  laki.seth(0)
   # laki.fd(20)
   laki.right(30)
def move_left():
   # laki.seth(180)
   # laki.fd(20)
   laki.left(30)
# def move_up():
  #  laki.seth(90)
   # laki.fd(20)
#def move_down():
 #   laki.seth(270)
  #  laki.fd(20)
s.listen()
s.onkey(move_right, 'Right')
s.onkey(move_left,'Left')
##3
while True:
    laki.fd(1)
    if laki.xcor()>270 or laki.xcor()<-270 or laki.ycor()>270 or laki.ycor()<-270:
        laki.right(180)
        Score=Score-5
        wr.clear()
        wr.write('امتیاز ='+ str(Score), font=('b koodak', 12,'bold'))
    if laki.distance(ball)<15:
        ball.goto(random.randint(-260,260),random.randint(-260,260))
        Score=Score+10
        wr.clear()
        wr.write('امتیاز ='+ str(Score), font=('b koodak', 12,'bold'))
    if Score>=50:
        wr.goto(-75,0)
        wr.write('شما موفق شدید', font=('b koodak',25,'bold'))
        break
while True:
 pass
