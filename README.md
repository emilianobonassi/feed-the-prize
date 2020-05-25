# feed-the-prize
Feed the PoolTogether prize (Hackathon: New York Blockchain Week)

It is a simple contract usefull for increase the prize of PoolTogether. When someone deposit `DAI`, using `feedPrize` function, the amount will be splitted, and a part is deposited into PoolTogether to increase the sponsored amount and another part is reserved to Idle Finance.

The sponsored amount earns interest but is not eligible to win, I choosed to use it instead 
to deposit for eligible tickets because i would like to prevent that the amount deposited to the contract could act some sort of monopolization of the prize. Instead the deposit into idle finance is useful to gain interests obtained by lending. I decided to use Idle for earn interests because it tries to maximaxe the return choosing the best APY.

Every time an user deposit or withdraw, the contract does some sort of rebalance between the amount deposited in PoolTogether and that into Idle. The amount in PoolTogether does not change, all the interests will be used for the week prize but the amount in idle is going to increase. If the two amount are balanced, the amount is going to divide 50%/50% between PoolTogether and Idle. The same behavior will be obtained if there is any amount left after a rebalance.

In a long run this contract could earn interests only using funds obtained by other interests. If users, in a future, withdraw all `DAI` deposited into this contract, it could continue to increase the week prize, forever.
