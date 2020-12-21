# Let-sVote

This is an experimental project, I tried to check: what if instead of using a huge, 
expensive and accurate neural net we will use a group of tiny cheap, and not so accurate neural nets.
The idea is based on the problem that in every dataset there are some extremities and when a single
neural net is trying to handle one extremity it forgets how to handle the other extremity. But,
when using a group of the neural net with a voting policy we don't need that every net will handle all the extremities.

As an example let's take the MNIST dataset: there are some 2s which are very close to 3s, there are some 3s which are very close to 8s 
and there are some 4s which are very close to 9s. One net must learn all the subtleties between (2,3),(3,8), and (4,9) but if we got 3 nets
every net can be mistaken in one subtlety.

Results: surprisingly(not really), the effectiveness of the method is depending on the parameters: number of neural nets, sizes of each layer in the neural nets.
The improvement between 3 net and one net is huge but if we take 100 nets we receive approximately the same result as three nets.
