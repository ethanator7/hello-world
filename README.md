# this is python 2.7
from random import randint
print "An easy stock exchange game"
print "Remember, the more you spend, the more you can lose"
stocks = {
	"bacon" : 10,
	"coffee" : 9,
	"cheese" : 7,
	"cereal" : 5,
	"tofu" : 2
}
for x in stocks:
	# this will print out all of the stocks with their costs
	print "%s stocks cost $%s" % (x, str(stocks[x]))
total_spent = 0
spending = {
	"bacon" : 0,
	"coffee" : 0,
	"cheese" : 0,
	"cereal" : 0,
	"tofu" : 0
}
stocking = {
	"bacon" : 0,
	"coffee" : 0,
	"cheese" : 0,
	"cereal" : 0,
	"tofu" : 0
}
for i in stocks:
	num_stocks = raw_input("How many %s stocks will you be investing in today?" % (i))
	total_spent += (num_stocks * stocks[i])
	num_spent = (num_stocks * stocks[i])
	print "%s %s stocks cost $%s" % (num_stocks, i, num_spent)
	print "total you have spent $%s" % (total_spent)
	spending[i] += num_spent
for t in spending:
	stocking[t] += (spending[t] * ((randint(1, 100) / 100) + .5))
	# this will multiply the amount spent on each stock by a number between .5 and 1.5, causing it to drop or rise up to 50%
stocking_total = 0
for v in stocking:
	stocking total += stocking[v]
change = total_spent - stocking_total
if change < 0:
	print "Congrats, you lost $%s" % (change)
elif change == 0:
	print "You didn't lose or make any money"
elif change > 0:
	print "Great job, you made $%s" % (change)
# not completed
