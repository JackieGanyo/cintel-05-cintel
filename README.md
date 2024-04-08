# cintel-05-cintel
# Module 5 Building Apps with Live Data &amp; Continuous Intelligence
#**Example as built during 5.2 Deques**
import plotly.express as px
from shiny.express import input, ui
from shinywidgets import render_plotly
from collections import deque

# Create an empty deque
empty_deque = deque()
print(empty_deque) 

# Create a deque by passing in a list with values
xchg_deque_F = deque( [18.7297, 18.6824, 19.1046, 19.7852, 18.2222] )
print(xchg_deque_F)  

#append elements from the deque
#append() method adds to the end of the deque
#appendleft() method adds to the beginning of the deque

xchg_deque_F.append(18.0000)
xchg_deque_F.appendleft(18.5000)
xchg_deque_F.append(19.8000)
xchg_deque_F.append(15.0000)
print(xchg_deque_F)

#Remove elements from the deque using pop() method
leftmost_element = xchg_deque_F.popleft()  
print ("leftmost element popped:", leftmost_element)
print ("Updated deque:", xchg_deque_F)

#Call the length of the deque
len(xchg_deque_F) 
print (len(xchg_deque_F))


# Initialize deque with a max length of 3 to store last 3 stock prices
msft_prices = deque(maxlen=3)

# Clear the deque (we might call this at the start of a new day)
msft_prices.clear()

# Simulate updating the stock price with new values
msft_prices.append(310.35)
print("MSFT stock prices:", list(msft_prices))

msft_prices.append(312.31)
print("MSFT stock prices:", list(msft_prices))

msft_prices.append(315.25)
print("MSFT stock prices:", list(msft_prices))

msft_prices.append(317.41)
print("MSFT stock prices:", list(msft_prices))

