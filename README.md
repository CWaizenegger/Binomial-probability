# Binomial-probability
Calculates the probability of a range of outcomes for testing within a binomial distribution.

function Px = BiProb(N,L,H,p) 
%Calculates the probability of a set of events occurring within a binomial
%situation

% N = total number of trials completed
% L = low bound on range to calculate probability within
% H = high bound on range to calculate probability within
% p = probability of positive result
% Px = probability that event x happens between L and H
Px = 0;

for i = L:H
    
    Px = Px + factorial(N)*(p^i)*(1-p)^(N-i)/(factorial(i)*factorial(N-i));
    
end
