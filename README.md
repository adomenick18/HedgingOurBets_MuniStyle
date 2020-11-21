# Hedging our Bets, Muni-style


## Background
### So what are muni-bonds?
Muni-bonds, more formally municipal bonds, are bonds issued by state and local governments to finance projects such as bridges, schools, transit systems, and community utilities. Municipal bonds are tax-free at the federal level and can be tax-free for holders who live in the state of issuance which makes them a common investment for banks as well as high net worth investors. These investments are the most prolific as far as the number of unique securities, but they can be very thinly traded versus other bonds and as a result are many times difficult to hedge for interest-rate risk (the risk of a decline in principal because of changes in interest rates.)
### How can we minimize interest-rate risk on municipal bonds?
One way to minimize the interest-rate risk on municipal bonds is to build a leveraged portfolio of bonds and simultaneously hedging the duration risk of the portfolio (source: Investopedia.) It is often challenging for investors to identify an appropriate hedge. Our project seeks to create a function that will identify the best hedge for a given bond and help users extrapolate that to apply to any municipal bond that they are trying to hedge.
## Data sets
For our sample of municipal bonds to test against, we identified 816 bonds from the overall universe of traded municipal bonds. We pulled over seven years of price data from Bloomberg again which to test our potential hedges.
The hedges that we selected to test against were MUB (a municipal bond ETF(exchange-traded fund,)) Treasuries, JNK (a high-yield bond ETF,) LQD (an intermediate-term corporate ETF,) UND (a dollar-index ETF,) and ICE LIBOR swaps. These are recognized hedges for municipal bonds. The Treasury bond data was pulled from Quandl, the ETF data from Alpaca and the ICE LIBOR data from Bloomberg.rate data for treasury bonds along with price data for ETF (exchange-traded funds)
## Methodology
Our team created a function in python to compare price correlation of the bonds versus the hedges. We sought to find the ones that had the closest correlation because since the hedge would be shorted, the hedge most closely tracked the bond price would result in the best hedge and protection against changes in interest rates.
##Results
Unfortunately we didn’t find a hedge that was very closely correlated to the bonds. Unsurprisingly, the strongest average correlation that we found was between the sample set and MUB (the municipal bond ETF.) This lack of a true conclusion speaks to what a hard problem that identifying hedges is to solve.
## Challenges
There were two main challenges that we faced while working on this project. First, the price data is reported differently between the bonds and some of the hedges. A great part of our team’s work was having the price data in a format where we could compare it apples-to-apples so we could run the correlation.  Another challenge that we faced was finding a way to capture the transaction costs of the hedges. We opted to ignore adding in the transaction costs for the purposes of our project. 
## Visualizations
While this project didn’t naturally lend itself to showing results in a visual format, we did create a dashboard of our findings. 
