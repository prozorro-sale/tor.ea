.. _bids:

Submit an offer by a participant
================================

After the participant has been logged in, he gets to the auction module page, where displayed  the buttons that are performance actions: increasing the current price and agreed with the current price.

Clicking on the corresponding button, results in different behavior of the auctions module.

The auction has a limit on the number of requests from the user transferred - 1 request / second.

Variations of button presses (clicks)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The participant clicked on the button `to Rise`
-----------------------------------------------

If a participant  presses the button "to rise", on the auction module page will appear a block with possible options of bid. Each proposed option on the list is greater than the price of the current round + minimalStep.amount, and multiple (aliquot) minimalStep.amount

When the amount is entered, the system accepts the transmitted value, 	
whereafter the current round is completed. Ending the round stops the timer.

The price of the next round is higher than the participant's bid for minimalStep.amount.

The participant clicked on the button `to accept`
-------------------------------------------------

In order for an auction to pass to the next round, it is necessary and sufficient for one participant to click on the "agree" button. With these actions, the current round is completed.

Ending the round stops the timer from the top.

The price of the next round is calculated automatically and is equal to the price of the previous round + minimalStep.amount.
