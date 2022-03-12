# Path-Signatures-and-ML
Building a simple classifier (based on linear regression) to determine whether a security is a cryptocurrency, stock, or an ETF just using a stream of price/volume data during pandemic trading. Inspired by a blog by Imanol Perez Arribas on path signatures Quantstart (see last item in bibliography from the Jupyter notebook), where the body of the code was adapted from. 

The idea is that the classifier should find some properties inherent to a given asset class. For example, prices of crypto are usually more volatile and activity in such assets boomed during the early pandemic. Then, ETFs should on average be more stable than single stocks etc. In a sense, each asset class should have its own staple, but the human eye probably won't be great at capturing it without sufficient context. 

Essentially, using path signatures rather than deep nets or other complex sequential models enables to only use relatively little data (around 1000 datapoints) but capture the most important properties. This is because truncation to a finite order works very well, with higher order terms having factorial decay. 
