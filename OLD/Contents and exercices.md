Derivatives

Christian Dorion Pascal Fran¸cois

_HEC Montreal HEC Montreal_

_& Fellow of the Canadian Derivatives Institute_

August 2025

PRELIMINARY DRAFT

ii

**Contents**

**Foreword vii**

#### 1 Fundamental notions 1

1.1 Main definitions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1

1.1.1 Derivative contract . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1

1.1.2 Forward contract . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1

1.1.3 Futures contract . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2

1.1.4 Basis . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 4

1.1.5 Options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 4

1.1.6 Hedging, speculation, and arbitrage . . . . . . . . . . . . . . . . . . . . . . . . . . . 7

1.2 Arbitrage with forwards . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 8

1.2.1 Absence of Arbitrage (AoA) . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 8

1.2.2 Forward price and spot price . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 8

1.2.3 Forward price and futures price . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 13

1.3 Arbitrage with options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 15

1.3.1 Bounds for the call premium . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16

1.3.2 Bounds for the put premium . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 17

1.3.3 Option values before maturity . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18

1.3.4 Parity and symmetry relations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 19

1.4 Hedging with derivatives . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 21

1.4.1 Hedging with forwards or futures . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 22

1.4.2 Hedging with options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 24

1.5 Speculative strategies using options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 26

1.5.1 Spreads . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 26

1.5.2 Combinations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 28

1.5.3 Butterflies, condors and other profiles . . . . . . . . . . . . . . . . . . . . . . . . . . 30

1.6 Problem set . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 31 1.7 Solutions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 35

#### 2 Diffusion model 47

2.1 Asset price dynamics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 47

2.2 The Brownian motion . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 50

iii

iv _CONTENTS_

2.3 Itˆo’s lemma . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 53

2.3.1 One-dimensional case . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 53

2.3.2 Itˆo’s product . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 55

2.3.3 Multi-dimensional case . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 55

2.4 Partial differential equation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 56

2.5 Risk-neutral approach . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 57

2.5.1 Intuition . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 57

2.5.2 Girsanov theorem . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 58

2.6 Feynman-Kac theorem . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 59

2.7 Problem set . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 61

2.8 Solutions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 62

#### 3 The Black-Merton-Scholes model 65

3.1 Solving the PDE . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 65

3.2 The martingale approach . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 66

3.3 Digital options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 68

3.4 Perpetual options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 69

3.5 Historical and implied volatilities . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 70

3.6 The market price of risk . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 72

3.7 Specific underlying assets . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 74

3.7.1 Options on forwards . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 74

3.7.2 Underlying asset with discrete dividends . . . . . . . . . . . . . . . . . . . . . . . . . 75

3.8 American options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 76

3.8.1 Quasi-analytical approximation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 76

3.8.2 Representation of the exercise frontier . . . . . . . . . . . . . . . . . . . . . . . . . . 79

3.8.3 Numerical comparison . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 81

3.9 Problem set . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 81 3.10 Solutions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 86

#### 4 Discrete-Time Approach 93

4.1 Standard binomial trees . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 93

4.1.1 CRR tree . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 94

4.1.2 Backward induction and the martingale property . . . . . . . . . . . . . . . . . . . . 95

4.1.3 Pricing algorithm . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 97

4.1.4 Convergence of the CRR tree to the BMS model . . . . . . . . . . . . . . . . . . . . 101

4.1.5 The Jarrow and Rudd parametrization . . . . . . . . . . . . . . . . . . . . . . . . . . 103

4.1.6 Convergence improvements . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 103

4.2 Expanded binomial trees . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 104

4.3 Trinomial trees . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 105

4.4 Replication . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 106

4.4.1 Greek parameters . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 107

4.4.2 Managing imperfect replication . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 115

4.5 Problem set . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 117

_CONTENTS_ v

4.6 Solutions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 121

#### 5 Exotic options 127

5.1 Barrier-type options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 127

5.1.1 Vanilla barrier options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 127

5.1.2 The reflection principle . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 130

5.1.3 Parisian options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 132

5.1.4 Double barrier options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 134

5.2 Average-type options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 134

5.2.1 Contract characteristics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 134

5.2.2 Asian option with geometric averaging . . . . . . . . . . . . . . . . . . . . . . . . . . 135

5.2.3 Asian option with arithmetic averaging . . . . . . . . . . . . . . . . . . . . . . . . . 136

5.3 Lookback options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 137

5.4 Spread options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 138

5.5 Compound options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 140

5.6 Options on the minimum or maximum of two assets . . . . . . . . . . . . . . . . . . . . . . 141

5.7 Miscellaneous exotic options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 143

5.7.1 Bermudian options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 143

5.7.2 Chooser options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 143

5.7.3 Shout options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 143

5.8 Problem set . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 144

5.9 Solutions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 150

#### 6 Numerical methods 159

6.1 Finite differences . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 159

6.1.1 Explicit method . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 159

6.1.2 Implicit methods . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 165

6.1.3 Crank-Nicolson algorithm . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 165

6.1.4 Numerical example . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 168

6.2 Monte Carlo simulations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 169

6.2.1 The simulation principle . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 169

6.2.2 Stochastic discounting . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 171 6.2.3 Correlated underlying assets . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 171 6.2.4 American options . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 173

6.2.5 Convergence improvements . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 176

6.3 Choosing the appropriate numerical method . . . . . . . . . . . . . . . . . . . . . . . . . . . 178

6.4 Problem set . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 178

6.5 Solutions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 182

#### 7 Modeling volatility 189

7.1 Implied volatility surface . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 190

7.2 GARCH models . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 194

7.2.1 Nonaffine GARCH(1,1) . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 195

vi _Derivatives, by Dorion and Fran¸cois, Sunday 24<sup>th</sup> August, 2025_

7.2.2 Properties of the model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 196

7.2.3 Other GARCH models . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 197

7.2.4 Parameter estimation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 198

7.2.5 Risk-neutralization . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 199

7.3 Stochastic volatility models . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 200

7.3.1 Hedging in the presence of stochastic volatility . . . . . . . . . . . . . . . . . . . . . 201

7.3.2 Some special cases . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 203

7.4 CEV models . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 206

7.5 Problem set . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 207

7.6 Solutions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 211

#### 8 Jump-diffusion models 217

8.1 Basics of the Poisson process . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 217

8.2 Some models with jumps . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 219

8.2.1 The (original) Merton model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 219

8.2.2 Priced jump risk . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 221

8.2.3 Discrete-time algorithm for American options . . . . . . . . . . . . . . . . . . . . . . 223

8.2.4 The Kou model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 224

8.2.5 Jump diffusion with stochastic volatility . . . . . . . . . . . . . . . . . . . . . . . . . 225

8.3 Simulating jump-diffusion models . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 226

**Foreword**

These teaching notes are a work in progress. Despite our careful revisions, this draft may not be exempt of typos, imprecisions or omissions. We are grateful to the readers who will help us spot them and improve the clarity of this document.

CD & PF

Montreal, August 2025.

vii

viii _Derivatives, by Dorion and Fran¸cois, Sunday 24<sup>th</sup> August, 2025_

**Chapter 1**

**Fundamental notions**

**1.1 Main definitions**

#### 1.1.1 Derivative contract

A derivative contract (or derivative product, or simply, a derivative) is a financial contract written on an underlying asset (UA). Its value is derived from that of the UA, hence the term _derivative_. The UA can be a stock, a corporate bond, a Treasury bond, an exchange rate, a commodity, or even another derivative.

In practice, derivatives can be used for hedging or speculation purposes. An economic agent is said to conduct a hedging operation when he or she aims at reducing the exposure of his or her wealth to a source of risk. By contrast, an economic agent is said to engage in speculation when he or she aims at increasing his or her wealth by taking advantage of the evolution of a source of risk. It is often hard to disentangle hedging from speculation. Some derivatives, especially option contracts, enable economic agents to partially hedge against a source of risk while leaving a certain exposure to speculation. The main categories of derivative contracts are: forwards, futures, options, and swaps.

#### 1.1.2 Forward contract

A forward contract is the firm commitment to buy (or sell) a given quantity of UA, at a given price, at a given time. The price specified in the contract is called the delivery price, or the forward price. It is determined in such a way that the value of the forward contract is nil at inception. In other words, entering into a forward is a transaction that does not cost anything to both parties.

We denote by _<sub>T</sub>_ the maturity date of the forward and by _<sub>K</sub>_ (_<sub>t</sub>_) the delivery price of the forward initiated at time _<sub>t</sub>_. The delivery price is set for the whole transaction. It must be distinguished from _<sub>f</sub>_ (_<sub>t,T</sub>_), the forward price calculated at time _<sub>t</sub>_, i.e., the delivery price with maturity date _<sub>T</sub>_ for a forward contract initiated at time _<sub>t</sub>_. At contract inception at time _<sub>t</sub>_, we must have

_K_ (_t_) = _f_ (_t,T_)_,_

and afterwards the forward price _<sub>f</sub>_ (_<sub>.,T</sub>_) may change over time while _<sub>K</sub>_ (_<sub>t</sub>_) remains fixed.

1

We denote by _<sub>S</sub>_(_<sub>t</sub>_) the market price of the UA. The financial position of the buyer of a forward contract is

_S_(_T_) _− K_ (_t_)_._

This position is called a long position, which means it gets more valuable as the price of the UA goes up.

Conversely, the financial position of the seller of a forward contract is

_K_ (_t_) _− S_(_T_)_,_

and this position is said to be short (it gets more valuable as the price of the UA goes down).

_K_

_S_

(

_T_

)

Payoff

Long forward

Short forward

_S_

(0)

Figure 1.1: Payoffs of long and short positions in a forward struck at _<sub>K</sub>_(_<sub>t</sub>_).

Upon maturity, the forward contract is settled either with the physical delivery of the UA (physical settlement) or with cash settlement (no asset is exchanged between the two parties, only the terminal value of the contract is transferred in cash).

### 1.1.3 Futures contract

The definition of a futures contract is similar to that of a forward contract with three notable differences.

**Exchange-traded contracts** Futures contracts are negotiated on exchange markets. They are therefore standardized (in terms of quality and quantity of UA, and in terms of available delivery dates) in order to be negotiated by a large number of investors. In other words, futures contracts are designed to be liquid. By contrast, forward contracts are bilateral agreements negotiated on over-the-counter (OTC) markets. The evolution of the futures price is subject to market constraints: a minimum variation called the tick and a maximum daily change.

**Clearing mechanism** The trading of futures contracts is overseen by an authority – the clearing house – that is responsible for the good execution of transactions on the organized market. Exposure to counterparty risk is considerably reduced for transactions on a futures market. This is because the clearing house acts as the counterparty for each trade (see Figure 1.2), and it requires that participating agents pay a deposit on a margin account to be allowed to trade (funds on margin accounts are usually capitalized using a monetary market rate).

Clearing house

buyssells buyssells

one contract one contract one contract one contract

|     |     |     |
| --- | --- | --- |
| Agent A Long position |     | Agent B<br><br>Short position |

Figure 1.2: Centrally-cleared transactions.

The net position of the clearing house is always nil. As far as trading agents are concerned, they can untie their position by taking the inverse position on a futures contract with same delivery date. In practice, a huge majority of futures contracts are untied before maturity.

**Mark-to-market** The position of each trading agent is updated on a daily basis. That is, on day _<sub>t</sub>_, the buyer of a futures receives (or pays, if negative)

_F_ (_t,T_) _− F_ (_t −_ ∆_t,T_)_,_

where _<sub>F</sub>_ (_<sub>t,T</sub>_) is the futures price at time _<sub>t</sub>_ and <sub>∆</sub>_<sub>t</sub>_ is the length of day (or the time elapsed since the last mark-to-market). The futures contract is said to be _marked-to-the-market_. To execute these daily settlements, trading agents use the funds initially deposited on the margin account. If, on a given day _<sub>t</sub>_, the mark-to-market requires that the trading agent must debit his or her margin account to a level below the minimum required level, the trading agent must replenish the margin account: this is the margin call. The amount of funds on the margin account must be reset to a certain level (that may be different from the initial required deposit). On some exchange markets, there is no minimum level and the margin call is executed every day. To reduce the opportunity cost, the trading agent is allowed to leave only the minimum required amount of funds on the margin account, and he or she can withdraw all funds in excess.

**Example 1.1** _On April 4, an agent buys a futures written on 100 units of UA, with a unit delivery price of <sub>K</sub>_ (_<sub>t</sub>_) = 365 _and a delivery date set to May 31. An initial deposit of 2,000 is required. The margin account is also subject to a minimum level of 1,500. The margin call must restore the account level to 2,000. The futures price evolves as follows_

_Date April 4 April 5 April 6 April 7 April 8_

_F_ (_<sub>t,T</sub>_) _365 362 359 364 367_

_On April 8, the agent unties his or her position by selling a futures with identical characteristics. His or her margin account will have fluctuated as follows_

_~~Date April 4 April 5 April 6 April 7 April 8~~_

_Mark-to-market_

(= 100\[_<sub>F</sub>_ (_<sub>t,T</sub>_) _− <sub>F</sub>_ (_<sub>t</sub> −_ <sub>∆</sub>_<sub>t,T</sub>_)\]) _0 -300 -300 +500 +300_

_Margin account_

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| _after mark-to-market_ | _0_ | _1,700_ | _1,400_ | _2,500_ | _2,300_ |
| _Cash withdrawal Margin account_ | _\-2,000_ | _0_ | _\-600_ | _500_ | _300_ |
| _after margin call_ | _2,000_ | _1,700_ | _2,000_ | _2,000_ | _2,000_ |

_On April 6, a margin call was executed to restore the margin account to 2,000._ □

### 1.1.4 Basis

The basis is defined as the difference between the futures price and the spot price, i.e.,

Basis = _F_ (_t,T_) _− S_(_t_)_._

In the absence of arbitrage, it must be that

_F_ (_T,T_) = _S_(_T_)_,_

that is, upon delivery date, the basis must be equal to zero, which is referred to as the basis _convergence_.

Before the delivery date, the basis can be either positive or negative. Later, we will examine the factors that determine the sign of the basis. Intuitively, this sign depends on the relative costs or benefits from physically holding the asset versus postponing its acquisition until maturity.

### 1.1.5 Options

An option is the right to buy (call option) or sell (put option) a given quantity of UA at a fixed price (the strike price) at or until a fixed date (the maturity date). When the exercise right is valid until maturity, options are said to be of American style. When it is valid only at maturity, options are said to be of European style.

Options are traded over the counter or on exchange markets. For a given type of UA, the style of option (American or European) that is traded on an exchange is referred to as the _vanilla_ option. For most types of UA, the vanilla option is the American option. Notable exceptions are index options and some currency options for which the vanilla option is the European option. Options traded on exchanges are standardized in terms of contract size (number of units of UA), available maturities (relatively few contracts are longer than a year), and available strike prices (the most traded options have a strike price close to the current price of the UA).

The buyer of an option pays a premium to the seller of the contract. This premium is paid at contract inception and compensates for the sold right, which, if exercised rationally, can have but a positive value.

We denote by _<sub>K</sub>_ the strike of the option. The payoff of the call option upon maturity is given by

max(_S_(_T_) _− K,_0)_,_

and is illustrated in Figure 1.3.

_K_

_S_

(

_T_

)

0

Payoff

Long one call

Figure 1.3: Terminal payoff of a call.

Similarly, the payoff of the put option upon maturity is given by

max(_K − S_(_T_)_,_0)_,_

and is illustrated in Figure 1.4.

_K_

_S_

(

_T_

)

0

Payoff

Long one put

Figure 1.4: Terminal payoff of a put.

At any time _<sub>t ≤ T</sub>_, the _moneyness_ of the option characterizes the monetary value that the option holder would get in case of immediate exercise. If this value is strictly positive (that is, if _<sub>S</sub>_(_<sub>t</sub>_) _<sub>\> K</sub>_ for a call or if _<sub>S</sub>_(_<sub>t</sub>_) _<sub>< K</sub>_ for a put), the option is in the money (ITM). If it is negative (that is, if _<sub>S</sub>_(_<sub>t</sub>_) _<sub>< K</sub>_ for a call or if _<sub>S</sub>_(_<sub>t</sub>_) _<sub>\> K</sub>_ for a put), the option out of the money (OTM). If it is nil (that is, if _<sub>S</sub>_(_<sub>t</sub>_) = _<sub>K</sub>_), the option is at the money (ATM).

The _intrinsic value_ of an option is the monetary value that the option holder would get in case of _rational_ immediate exercise. Thus,

Call intrinsic value = max(0_<sub>,S</sub>_(_<sub>t</sub>_) _− <sub>K</sub>_)_<sub>,</sub>_ Put intrinsic value = max(0_<sub>,K</sub> − <sub>S</sub>_(_<sub>t</sub>_))_<sub>.</sub>_

By construction, the difference between the actual value of the option and its intrinsic value is the value stemming from the possibility to postpone the exercise of the option. It is called the _speculative value_ (or time value) and therefore we can write

Option value = Intrinsic value + Speculative value.

Without any need for a model, we can intuitively determine some factors that influence the premium of an option. These factors are: the price of the UA (_<sub>S</sub>_), the option strike (_<sub>K</sub>_), the option maturity date (_<sub>T</sub>_), the risk-free interest rate (_<sub>r</sub>_), the dividend rate of the UA (_<sub>y</sub>_), and the “variability” (defined in a broad sense for now) of the UA price (_<sub>σ</sub>_). The sensitivities of the option premium to these factors are given in the table below.

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
| Factor | European call | European put | American call | American put |
| _S_ | +   | _−_ | +   | _−_ |
| _K_ | _−_ | +   | _−_ | +   |
| _T_ | ?   | ?   | +   | +   |
| _r_ | +   | _−_ | +   | _−_ |
| _y_ | _−_ | +   | _−_ | +   |
| _σ_ | +   | +   | +   | +   |

The effects of _<sub>S</sub>_ and _<sub>K</sub>_ are directly derived from the expression of the intrinsic value of the option. The positive effect of _<sub>σ</sub>_ can be explained by the convexity of the option payoff (see Figures 1.3 and 1.4). All else equal, more variability of the UA price increases the likelihood of extreme realizations of _<sub>S</sub>_. For a call (put), a realization more at the left-hand (right-hand) side of the UA price distribution does not marginally change the option value, because the terminal payoff remains equal to zero. However, a realization more at the right-hand (left-hand) side of the UA price distribution improves the option payoff. The net effect of increased UA price variability is therefore positive.

The factor _<sub>r</sub>_ directly measures the discounting effect. It has a positive (negative) impact on the call (put) premium because the holder of the call (put) option pays (receives) the strike price in case of future exercise. By contrast, the factor _<sub>y</sub>_ measures the benefits from holding the UA. These dividends induce automatic drops in the UA ex-dividend price. As long as the option is not exercised, these price drops benefit the holder of the put option but not the holder of the call option.

The effect of _<sub>T</sub>_ is the combined effects of _<sub>r</sub>_, _<sub>y</sub>_, and _<sub>σ</sub>_. An option with longer maturity has a greater speculative value (captured through the factor _<sub>σ</sub>_), while the discount factor plays positively (negatively) for the call (put), and while the dividend factor plays negatively (positively) for the call (put). When all these effects are put together, the net effect of a longer maturity on the premiums of European options is ambiguous. Admittedly, it is most likely positive for European calls unless the dividend effect more than offsets the combined discount and speculative effects. Furthermore, it is most likely positive for European puts unless the discount effect more than offsets the combined dividend and speculative effects. Note that the maturity effect is inversely related to the effect of the passage of time (i.e., time to maturity decreases as _<sub>t</sub>_ increases). Thus, call options usually lose value as time goes by (they are “decaying” assets), while the opposite usually holds for put options.

Finally, the net impact of discount, dividend, and speculative effects on American option premiums can only be but positive. This is precisely because the holder of the American option can put an end to the contract when he or she wants. The trade-off between these three effects will in particular determine the optimal early exercise of the American option. When the net impact of discount, dividend, and speculative effects become negative as time goes by, it is the right moment for the American option holder to exercise and terminate the contract.

### 1.1.6 Hedging, speculation, and arbitrage

The motives for trading derivatives can be grouped in three categories.

**Hedging motive** Consider an agent with a financial or commercial position that is exposed to variations of the UA price. The agent acts as a hedger if he or she wishes to reduce this risk exposure. Typical hedgers are corporations willing to manage their exposure to currency risk and/or interest rate risk. Companies in the agricultural, mining or energy sectors are also interested in reducing their exposure to commodity price risk (oil, metals, cereals...). Financial institutions and insurance companies may wish to hedge the value of their financial investments by trading derivatives on financial assets (indices, stocks, bonds...). What all these agents have in common is a hedging strategy: the derivatives trade yields a position that is opposite to the initial (financial or commercial) position. The resulting net position is less impacted by variations in the UA price as the gain (loss) on the initial position is at least partially offset by the loss (gain) on the hedge position.

**Speculative motive** Speculators are agents that wish to benefit from expectations they build about future asset prices. These expectations can be grounded on economic analysis, market judgment, or simply intuition. A speculative strategy consists in taking a position that will gain value if the agent’s anticipations turn out to be right. As opposed to the hedging strategy, it is, by definition, a risk-taking strategy. Derivatives are, by construction, good vehicles for speculative strategies because of their _leverage_ effect. In other words, with a relatively small amount invested, a position in a derivative can yield substantial gains or losses. Speculation using forwards or futures entails the highest leverage effect because the initial investment is nil (or close to zero if we take into account the opportunity cost of funds deposited in the margin account). But the speculative strategies using forwards or futures are not very sophisticated because these derivative payoffs are linear and therefore can only address basic anticipations (such as “the price will go up” or “the price will go down”). By contrast, speculative strategies using options may cost a few premiums but their payoff profile is much more flexible and can be tailored to address more complex anticipations. Option-based speculative strategies will be examined in greater detail in section 1.5.

**Arbitrage motive** The goal of arbitrageurs is to generate (almost) riskless profits by taking advantage of irregularities in market prices. Derivatives are important tools for arbitrageurs because their contractual definition establishes a link between their price and the UA price. When these model-free relations between the derivative price and its UA price are not observed in the market, arbitrageurs seize this arbitrage opportunity and generate a profit. As will be explained further, the activity of arbitrageurs is disciplining the market in that it contributes to maintaining these relations in equilibrium.

## 1.2 Arbitrage with forwards

In this section and the following, we examine the relations that must prevail between derivatives and their UA in the absence of arbitrage opportunity. This section is devoted to forward and futures while the next one deals with options. The assumption of Absence of Arbitrage (AoA) is explained first. Then we study the relation between the forward price and the spot price, and the relation between the futures price and the forward price.

### 1.2.1 Absence of Arbitrage (AoA)

An arbitrage opportunity is a zero-cost strategy with a non-trivial probability of generating a strictly positive gain in the future. In other words, arbitrage is the possibility to create value out of nothing. When the financial market is assumed to be frictionless (i.e., no transaction costs, no restrictions on short selling, no taxes) and competitive (i.e., all agents are price-takers), it is possible to derive the no-arbitrage price for some standard (“plain vanilla”) derivatives. These no-arbitrage prices essentially reflect the contractual relation between the derivative and its UA.

In practice, no-arbitrage prices are enforced by the intervention of _arbitrageurs_. These agents take advantage of a temporary difference between the observed price and the no-arbitrage price by implementing a strategy commonly referred to as “buying at the low and selling at the high”. That is, arbitrageurs take a joint position in the derivative and its UA, and buy the security which is undervalued relative to the other while selling the other one. With this strategy, arbitrageurs cash in an immediate profit and make sure that their positions in the derivative and its UA will cancel out in the future (typically upon the maturity of the derivative).

We derive no-arbitrage price relations by invoking the absence of arbitrage (AoA). Arbitrageurs contribute to the strength of this assumption since their interventions make arbitrage opportunities disappear quickly. Indeed, arbitrageurs put a strong buy pressure on the relatively undervalued security and a strong sell pressure on the relatively overvalued security until these two securities (the derivative and its UA) exhibit prices that are consistent with the AoA.

### 1.2.2 Forward price and spot price

To clarify the exposition, we present some no-arbitrage relations using the simple (not compounded) interest rate _<sub>i</sub>_ to compute interests from money market operations. Next, we will generalize these relations by using the continuously compounded interest rate _<sub>r</sub>_.

##### Underlying asset without dividends

The following strategy allows to determine the forward price under the AoA. It is referred to as the _cash and carry_ strategy. At initial date, an investor builds the following portfolio

###### Transaction Cash flow

Buying one unit of the UA _<sub>−S</sub>_(0)

Borrowing _<sub>S</sub>_(0) at the risk-free rate +_<sub>S</sub>_(0) Selling one forward contract 0 0 Upon delivery date _<sub>T</sub>_, the portfolio is worth

Net cash flow

Transaction Position

Long one unit of the UA _<sub>S</sub>_(_<sub>T</sub>_) Paying back the loan _<sub>−S</sub>_(0)(1 + _<sub>iT</sub>_)

Short one forward contract _<sub>f</sub>_ (0_<sub>,T</sub>_) _− <sub>S</sub>_(_<sub>T</sub>_)

###### Net position _<sub>f</sub>_ (0_<sub>,T</sub>_) _− <sub>S</sub>_(0)(1 + _<sub>iT</sub>_)

Under the AoA, the portfolio (whose initial cost was nil) must be worth nothing at date _<sub>T</sub>_. Consequently, we obtain the following proposition.

**Proposition 1.2** _(Basic cash and carry relation) Under the AoA, the forward price at time_ 0 _of the UA without dividends is given by_

_f_ (0_<sub>,T</sub>_) = _<sub>S</sub>_(0)(1 + _<sub>iT</sub>_)_<sub>,</sub>_ (1.1)

_or, put differently,_

_f_ (0_,T_) _− S_(0) = _S_(0)_iT,_

_which means that the basis equals the UA’s cost of carry._

**Example 1.3** _The stock of the company FGH is worth $100. The 3-month forward price of this stock is $100.8. The 3-month risk-free rate is 4%. How to take advantage of an arbitrage opportunity? The arbitrageur short sells the stock, lends the $100 for three months, and buys one forward contract. Three months later, the arbitrageur uses the forward contract to buy the FGH stock at $100.8 and close the short selling position. He or she is paid back from the loan and receives_ 1001 + 0_<sub>.</sub>_04<sub>12</sub><sup>3</sup> \= $101_. He or she therefore cashes in a net profit of_

101 _−_ 100_<sub>.</sub>_8 = 0_<sub>.</sub>_2_<sub>,</sub>_

_that is 20 cents per stock. This arbitrage strategy is called a reverse cash and carry. Notice that short selling must be authorized to implement the reverse cash and carry strategy._ □ **Underlying asset with dividends**

Dividend payments impact on the relation between the spot and the forward prices. Indeed, a long position in the forward allows to acquire the UA upon the delivery date _<sub>T</sub>_, but it does not give right to interim payments such as dividends until _<sub>T</sub>_.

Suppose the UA pays the dividends _d_(_t<sub>j</sub>_) at dates (_t<sub>j</sub>_)_<sub>j</sub>_<sub>\=1</sub>_<sub>,...,n</sub>_ with _t_<sub>1</sub> _< t_<sub>2</sub> _< ... < t<sub>n</sub> ≤ T_. When dividends are known with certainty, Proposition 1 can be readily generalized. Consider the following two strategies.

Strategy 1

Transactions Cash flow

Buying one unit of the UA _<sub>−S</sub>_(0)

Borrowing the discounted _d_(_tj_) until _tj_ +P_nj_\=1 1+_d_(_titj_)_j_

Net cash flow _−S_(0) + P_nj_\=1 1+_d_(_titj_)_j_

|     |     |
| --- | --- |
| Strategy 2 |     |
| ~~Transactions~~ | ~~Cash flow~~ |
| Buying one forward contract | 0   |
| Lending _<sub>f</sub>_ (0_<sub>,T</sub>_)_<sub>/</sub>_(1 + _<sub>iT</sub>_) at the risk-free rate until _<sub>T</sub>_ | _−f_(0_,T_) |
| Net cash flow | 1+_iT_<br><br>_−f_1+(0_,TiT_) |

At date _<sub>T</sub>_, strategy 1 is worth _<sub>S</sub>_(_<sub>T</sub>_) as all dividends received were used to pay back every loan. Strategy 2 is also worth _<sub>S</sub>_(_<sub>T</sub>_). Indeed, the forward contract yields a position _<sub>S</sub>_(_<sub>T</sub>_)_<sub>−f</sub>_ (0_<sub>,T</sub>_) and the loan yields an inflow of _<sub>f</sub>_ (0_<sub>,T</sub>_). Under the AoA, these two strategies must therefore have the same value at initial date, which yields the next proposition.

**Proposition 1.4** _(Cash and carry relation for dividend-paying assets) Under the AoA, the forward price at date_ 0 _of the UA paying the dividends <sub>d</sub>_(_<sub>tj</sub>_) _at dates <sub>tj</sub> is given by_

_f_ (0_,T_) = _S_(0) _−_ X_n_ 1 +_d_(_titj_)_j ,_ (1.2)

1 + _iT j_\=1

_or, put differently,_

(0_,T_) _− S_(0) = _S_(0)_iT −_ X_n d_ 1 + _iT f_ (_tj_) 1 + _it ,_

_j_\=1 _j_

_which, again, means that the basis equals the UA’s (net) cost of carry._

**Example 1.5** _Consider a Treasury bond maturing in two years quoted at $100. It offers a coupon of $8 in three months. What is the bond’s 6-month forward price, given that the 3-month and 6-month risk-free rates are 4% and 5%, respectively? From equation (1.2), we obtain_

0_,_ 12 \= 1 + 0_._<sup>05</sup>126 100 _−_ 12 <sup>!</sup> \= 94_._38_,_

_f_

_hence a forward price of $94.38._ □ **Currency forward**

Consider a foreign currency, say the British pound (_£_), and let _<sub>i£</sub>_ denote the foreign money market risk-free rate. In this case, the underlying “asset” _<sub>S</sub>_(_<sub>t</sub>_) represents the exchange rate between the domestic and the foreign currencies. It is convenient to define _<sub>S</sub>_(_<sub>t</sub>_) as the direct quote, that is, the number of units of domestic currency that can be exchanged for one unit of foreign currency. Consider the following strategy

|     |     |
| --- | --- |
| ~~Transactions~~ | ~~Cash flow (in $)~~ |
| Borrowing <sup>1</sup> units of foreign currency until | \+ _S_(0) |

_<sub>T</sub>_

<sub>1+</sub>_<sub>i£</sub>T_ <sub>1+</sub>_<sub>i£</sub>T_

Lending _f_1+(0_,TiT_) dollars until _T −f_1+(0_,TiT_)

Net cash flow 1+_S_(0)_i£T − f_1+(0_,TiT_)

Upon delivery date, this strategy is worth _<sub>f</sub>_ (0_<sub>,T</sub>_) _<sub>− S</sub>_(_<sub>T</sub>_) and thus replicates the short position in the forward contract. Under the AoA, the initial value of this strategy must be nil, which yields:

**Proposition 1.6** _(Cash and carry relation for currencies) Under the AoA, the forward exchange rate at date_ 0 _between the dollar and the pound is given by_

_f_ (0_,T_) = _S_(0)1 +1 +_iiT£T ,_ (1.3)

_or, put differently,_

_f_ (0_,T_) _− <sub>S</sub>_(0) = _S_(0)<sup>(</sup>_<sup>i</sup>_1 +_<sup>− i£</sup>_)_T ,_

_i<sub>£</sub>T_

_which indicates that the difference in interest rates drives the discount or the premium of the foreign currency against the domestic currency (a result known as the covered interest rate parity)._

**Example 1.7** _The 1-month risk-free rates are 5% in the domestic country and 6% in the foreign country. The spot exchange rate is £1 = $1.54. What is the no-arbitrage 1-month forward exchange rate? Applying formula (1.3) yields f_ (0_<sub>,</sub>_1_<sub>/</sub>_12) = 1_<sub>.</sub>_54= 1_<sub>.</sub>_5387_<sub>,</sub>_

12 _hence the foreign currency trades at a slight discount against the domestic currency._ □

##### Commodity forward

Commodities underlying futures contracts can be classified into three complexes: Agricultural (e.g., grains, livestock, dairy), energy (e.g., crude oil, natural gas, electricity) and metals (e.g., gold, copper, platinum). Some commodities (like gold or cereals) imply significant storage costs. By contrast, some other commodities (like copper or oil) are associated with benefits for their holder, in particular because these commodities are used as investment inputs to create value in the real economy. These costs or benefits from holding the commodity are referred to as the convenience value or convenience yield if expressed in relative terms. We will use the notion of convenience yield in a net sense, that is, a negative convenience yield means that the costs of carrying the underlying more than offset the benefits from holding it.

The convenience yield clearly impacts on the relation between the spot and the forward prices. Indeed, buying a forward contract allows to acquire the underlying commodity upon maturity thereby missing the convenience value (positive or negative) from initial date until _<sub>T</sub>_.

One way to adjust the cash and carry relation for commodities is to express the convenience yield as a continuous rate _<sub>y</sub>_. This implies that the position consisting in holding one unit of the commodity at date 0 will appreciate over time so that it becomes equivalent to holding exp(_<sub>yt</sub>_) units of the commodity at date _<sub>t</sub>_. This appreciation at rate _<sub>y</sub>_ is obtained by reinvesting the proceeds from holding the commodity into the position.

Now consider the following strategy. For consistent discounting rules, we now use the continuously compounded risk-free rate _<sub>r.</sub>_ At initial date,

|     |     |
| --- | --- |
| Transaction<br><br>~~Buying exp(~~_<sub>−yT</sub>_~~) units of the UA~~ | Cash flow _−S_~~(0)exp(~~_−yT_~~)~~ |
| Borrowing _<sub>S</sub>_(0)exp(_−<sub>yT</sub>_) until _<sub>T</sub>_ | +_S_(0)exp(_−yT_) |
| Selling one forward contract | 0   |
| Net cash flow | 0   |

Upon delivery date _<sub>T</sub>_, the portfolio is worth

Position

Transaction

Long in _one_ unit of the UA _<sub>S</sub>_(_<sub>T</sub>_)

(because of the appreciation of the position at rate _<sub>y</sub>_)

Paying back the loan _−<sub>S</sub>_(0)exp(_−<sub>yT</sub>_)exp(_<sub>rT</sub>_)

Short one forward contract _<sub>f</sub>_ (0_<sub>,T</sub>_) _− <sub>S</sub>_(_<sub>T</sub>_)

~~Net position~~ _<sub>f</sub>_ ~~(0~~_<sub>,T</sub>_~~)~~ _− <sub>S</sub>_~~(0)exp\[(~~_<sub>r</sub> − <sub>y</sub>_~~)~~_<sub>T</sub>_~~\]~~

Under the AoA, the portfolio (whose initial cost was nil) must be worth nothing at date _<sub>T</sub>_.

**Proposition 1.8** _(Generalized cash and carry relation) Under the AoA, the spot and forward prices at any time <sub>t < T</sub> are linked through the following relation_

_f_ (_t,T_) = _S_(_t_)exp\[(_r − y_)(_T − t_)\]_,_ (1.4)

_where <sub>r</sub> stands for the risk-free rate and <sub>y</sub> for the convenience yield of the underlying asset, both continuously compounded._

The generalized cash and carry relation may be applied to a wide variety of underlying assets, provided that the rate _<sub>y</sub>_ be reinterpreted accordingly. As we mentioned earlier, when it comes to commodities, the rate _<sub>y</sub>_ is naturally interpreted as the convenience yield. But the rate _<sub>y</sub>_ can also be seen as the continuous dividend yield when the underlying asset is a stock index. It represents the foreign continuously compounded risk-free rate when equation (1.4) is applied to currency forwards.

### 1.2.3 Forward price and futures price

No arbitrage relations can be established between the forward price and the futures price of the same underlying asset. In this subsection we report results initially derived by Cox et al. (1981) and Jarrow and Oldfield (1981). Let _<sub>B</sub>_ (_<sub>t,T</sub>_) denote the relevant discount factor between date _<sub>t</sub>_ and date _<sub>T</sub>_. Consistent with our previous notations, the discount factor can be expressed with the simple, discrete money market rate _<sub>i</sub>_

_B_ (_t,T_) =_._

Alternatively, the discount factor _<sub>B</sub>_ (_<sub>t,T</sub>_) is the value at time _<sub>t</sub>_ of the zero-coupon bond with nominal $1 and maturity date _<sub>T</sub>_, which can be expressed with the continuously compounded risk-free rate _<sub>r</sub>_

_B_ (_t,T_) = exp\[_−r_(_T − t_)\]_._

**Lemma 1.9** _The forward price <sub>f</sub>_ (0_<sub>,T</sub>_) _is the value at time 0 of a contract that pays off <sub>S</sub>_(_<sub>T</sub>_)_<sub>/B</sub>_ (0_<sub>,T</sub>_) _at time <sub>T</sub>._

Proof: Consider the following strategy.

##### ~~Transactions Cash flow~~

Buying 1_<sub>/B</sub>_ (0_<sub>,T</sub>_) forward contracts 0

|     |     |
| --- | --- |
| Lending _<sub>f</sub>_ (0_<sub>,T</sub>_) until _<sub>T</sub>_ | _−f_ (0_,T_) |
| Net cash flow<br><br>Upon delivery date, we obtain | _−f_ (0_,T_) |

Transactions Position

~~Long in 1~~_/B_ ~~(0~~_,T_~~) forward contracts~~ _<sub>B</sub>_<sub>(0</sub><sup>1</sup>_<sub>,T</sub>_<sub>)</sub> ~~(~~_S_~~(~~_T_~~)~~ _− f_ ~~(0~~_,T_~~))~~

Payback of loan +_Bf_(0(0_,T,T_))

Net position +_BS_(0(_T,T_))

|     |     |
| --- | --- |
| which ends the proof. | □   |

**Lemma 1.10** _The futures price F_ (0_,T_) _is the value at time 0 of a contract that pays off S_(_T_)<sup>Q</sup>_<sup>N</sup><sub>n</sub>_<sub>\=0</sub>_<sup>−</sup>_<sup>1</sup> (1 + _i<sub>n</sub>_) _where <sub>N</sub> is the number of days (of length_ <sub>∆</sub>_<sub>t</sub>_ \= _<sub>T/N</sub>) between 0 and <sub>T</sub>, and the collection of <sub>in</sub> represents_

|     |     |
| --- | --- |
| _daily, not annualized risk-free rates at time <sub>tn</sub>_ \= _<sub>n</sub>_<sub>∆</sub>_<sub>t</sub>._<br><br>Proof: Consider the following strategy |     |
| ~~Transactions on day~~ _<sub>t</sub>_<sub>0</sub> ~~\= 0~~ | ~~Cash flow~~ |
| Buying 1 + _<sub>i</sub>_<sub>0</sub> futures contracts | 0   |
| Lending _<sub>F</sub>_ (0_<sub>,T</sub>_) until _<sub>t</sub>_<sub>1</sub> | _−F_ (0_,T_) |
| Net cash flow | _−F_ (0_,T_) |

On the next day _<sub>t</sub>_<sub>1</sub> (and so on until day _<sub>tN−</sub>_<sub>1</sub>)

|     |     |
| --- | --- |
| Transactions on day _<sub>t</sub>_<sub>1</sub> | Cash flow |
| Paying back the former loan | +_F_ (0_,T_)(1 + _i_<sub>0</sub>) |
| Rolling over the former loan until day _<sub>t</sub>_<sub>2</sub> | _−F_ (0_,T_)(1 + _i_<sub>0</sub>) |
| Selling the former 1 + _<sub>i</sub>_<sub>0</sub> futures contracts | (1 + _i_<sub>0</sub>)(_F_ (_t_<sub>1</sub>_,T_) _− F_ (0_,T_)) |
| Lending the margin until day _<sub>t</sub>_<sub>2</sub> | _−_(1 + _i_<sub>0</sub>)(_F_ (_t_<sub>1</sub>_,T_) _− F_ (0_,T_)) |
| Buying (1 + _<sub>i</sub>_<sub>0</sub>)(1 + _<sub>i</sub>_<sub>1</sub>) futures contracts | 0   |
| Net cash flow | 0   |

Upon delivery date, the strategy is liquidated. Rolling over the initial loan of _<sub>F</sub>_ (0_<sub>,T</sub>_) yields the cash flow _<sub>F</sub>_ (0_<sub>,T</sub>_)<sup>Q</sup>_<sup>N</sup><sub>n</sub>_<sub>\=0</sub>_<sup>−</sup>_<sup>1</sup> (1 + _<sub>in</sub>_). As far as the positions on futures contracts are concerned:

- Buying at 0 and selling on the next day (1 + _<sub>i</sub>_<sub>0</sub>) futures contracts generates the margin

(1 + _i_<sub>0</sub>)(_F_ (_t_<sub>1</sub>_,T_) _− F_ (0_,T_))_,_

which is rolled over from day _t_<sub>1</sub> till _t<sub>N</sub>_ \= _T_ to yield (_F_ (_t_<sub>1</sub>_,T_) _− F_ (0_,T_))<sup>Q</sup>_<sub>n</sub><sup>T</sup>_<sub>\=0</sub>_<sup>−</sup>_<sup>1</sup> (1 + _i<sub>n</sub>_)_._

- Buying at day _<sub>t</sub>_<sub>1</sub> and selling on the next day (1 + _<sub>i</sub>_<sub>0</sub>)(1 + _<sub>i</sub>_<sub>1</sub>) futures contracts generates the margin

(1 + _i_<sub>0</sub>)(1 + _i_<sub>1</sub>)(_F_ (_t_<sub>2</sub>_,T_) _− F_ (_t_<sub>1</sub>_,T_))_,_

which is rolled over from day _t_<sub>2</sub> till _T_ to yield (_F_ (_t_<sub>2</sub>_,T_) _− F_ (_t_<sub>1</sub>_,T_))<sup>Q</sup>_<sup>N</sup><sub>n</sub>_<sub>\=0</sub>_<sup>−</sup>_<sup>1</sup> (1 + _i<sub>n</sub>_)_._

- ...
- Buying at day _<sub>tN−</sub>_<sub>2</sub> and selling on the next day (1 + _<sub>i</sub>_<sub>0</sub>)(1 + _<sub>i</sub>_<sub>1</sub>)_<sub>...</sub>_(1 + _<sub>iN−</sub>_<sub>2</sub>) futures contracts generates the margin
    1.  \+ _i_<sub>0</sub>)(1 + _i_<sub>1</sub>)_..._(1 + _i<sub>T−</sub>_<sub>2</sub>)(_F_ (_t<sub>N−</sub>_<sub>1</sub>_,T_) _− F_ (_t<sub>N−</sub>_<sub>2</sub>_,T_))_,_

which is rolled over till _T_ to yield (_F_ (_t<sub>N−</sub>_<sub>1</sub>_,T_) _− F_ (_t<sub>N−</sub>_<sub>2</sub>_,T_))<sup>Q</sup>_<sup>N</sup><sub>n</sub>_<sub>\=0</sub>_<sup>−</sup>_<sup>1</sup> (1 + _i<sub>n</sub>_)_._

- Buying at day _<sub>tN−</sub>_<sub>1</sub> a number of (1 + _<sub>i</sub>_<sub>0</sub>)(1 + _<sub>i</sub>_<sub>1</sub>)_<sub>...</sub>_(1 + _<sub>iT−</sub>_<sub>1</sub>) futures contracts generates at time _<sub>T</sub>_ the margin
    1.  \+ _i_<sub>0</sub>)(1 + _i_<sub>1</sub>)_..._(1 + _i<sub>T−</sub>_<sub>1</sub>)(_F_ (_T,T_) _− F_ (_t<sub>N−</sub>_<sub>1</sub>_,T_))_,_

that is, the cash flow (_F_ (_T,T_) _− F_ (_t<sub>N−</sub>_<sub>1</sub>_,T_))<sup>Q</sup>_<sup>N</sup><sub>n</sub>_<sub>\=0</sub>_<sup>−</sup>_<sup>1</sup> (1 + _i<sub>n</sub>_).

Consequently, the strategy generates no interim cash flow and a terminal net cash flow given by

_N−_1 _N−_1 _N−_1

_F_(0_,T_) <sup>Y</sup> (1 + _i<sub>n</sub>_) + <sup>X</sup> (_F_ (_t<sub>n</sub>_<sub>+1</sub>_,T_) _− F_ (_t<sub>n</sub>,T_)) <sup>Y</sup> (1 + _i<sub>n</sub>_)

_n_\=0 _n_\=0 _n_\=0

_N−_1 " _N−_1 #

\= <sup>Y</sup> (1 + _i<sub>n</sub>_) _F_ (0_,T_) + <sup>X</sup> (_F_ (_t<sub>n</sub>_<sub>+1</sub>_,T_) _− F_ (_t<sub>n</sub>,T_))

_n_\=0 _n_\=0

_N−_1

\= <sup>Y</sup> (1 + _i<sub>n</sub>_)\[_F_ (_T,T_)\]

_n_\=0 _N−_1

\= <sup>Y</sup> (1 + _i<sub>n</sub>_)_S_(_T_)_,_

_n_\=0

the last equality stemming from the convergence of the basis.□

Combining the two lemmas, we obtain the following proposition.

**Proposition 1.11** _When interest rates are not stochastic, then, in the absence of counterparty risk and market frictions, forward and futures prices are the same_

_f_ (_t,T_) = _F_ (_t,T_) _∀t,∀T._

**Proof** With non-stochastic interest rates,

(01_,T_) = _Nn_Y=0_−_1 (1 + _in_)_, B_

hence the two strategies examined in the former two lemmas must have the same initial cost under the AoA.□

The proposition entails that the stochastic nature of interest rates is one important driver of the difference between forward and futures prices. Other factors may also explain this difference, such as counterparty and illiquidity risks (much more important in the case of forward positions), or liquidity constraints induced by margin calls on futures positions.

## 1.3 Arbitrage with options

Let _<sub>c</sub>_(_<sub>t,T,K</sub>_) and _<sub>C</sub>_ (_<sub>t,T,K</sub>_) denote the premiums of the European and American call options written on the UA that is currently worth _<sub>S</sub>_(_<sub>t</sub>_), with maturity date _<sub>T</sub>_ and strike price _<sub>K</sub>_. Notations _<sub>p</sub>_(_<sub>t,T,K</sub>_) and _<sub>P</sub>_ (_<sub>t,T,K</sub>_) apply for the European and American puts in a similar fashion. Whenever relevant to the valuation of option _<sub>O</sub>_, we will highlight one particular value _<sub>x</sub>_ taken by a state variable using the notation

_O_(_t,T,K |S_(_t_) = _x_).

Without any loss in generality, the UA is assumed to generate a continuous dividend at rate _<sub>y</sub>_. As mentioned earlier, the rate _<sub>y</sub>_ is to be economically interpreted according to the nature of the underlying. It is the convenience yield for commodity options. It is the foreign risk-free rate for currency options. It is the domestic risk-free rate for options on forwards. To understand the latter interpretation, recall from the generalized cash and carry relation that the forward contract can be viewed as a dividend-paying spot asset provided the dividend yield is exactly set equal to _<sub>r</sub>_. Most of the no-arbitrage relations covered in this chapter were initially presented in Merton (1973).

### 1.3.1 Bounds for the call premium

**Proposition 1.12** _Under the AoA, the following holds_

|     |     |
| --- | --- |
| _C_ (_t,T,K \|S_(_t_) = 0) = 0_,_ | (1.5) |
| _C_ (_t,T,K_) _≥_ max(_S_(_t_) _− K,_0)_,_ | (1.6) |
| _C_ (_t,T,K_) _≤ S_(_t_)_,_ | (1.7) |

_c_(_t,T,K_)_,_ (1.8)

_C_ (_t,T,K_) _≥ c_(_t,T,K_)_._ (1.9)

**Proofs** The UA price reflects the discounting of the UA future value. So if the price is currently nil, it means that the financial market expects it to remain at zero in the future. Thus, given the absence of any upside potential, equation (1.5) holds.

When the intrinsic value is positive, the holder of the American call can capture it by immediate exercise. Hence, if equation (1.6) were not true, buying the American call and exercising it at once would be an arbitrage opportunity.

Suppose the UA price is strictly lower than the American call premium. Then an arbitrage strategy consists in an investor buying the UA and selling the American call. Indeed, this yields an initial strictly positive cash flow for the investor. In the future, either the call is exercised and the investor can deliver the UA and cash in the strike price (yielding a strictly positive cash flow), or the call is not exercised and the investor remains long in the UA. Barring arbitrage, it must therefore be that equation (1.7) holds.

Let us prove equation (1.8) in two steps. First, the European call is an option so its value cannot be negative. Next, suppose that

_c_(_t,T,K_) _< S_(_t_)_e−y_(_T−t_) _− Ke−r_(_T−t_)_,_

and consider the following strategy: Short selling _<sub>e</sub><sup>−y</sup>_<sup>(</sup>_<sup>T−t</sup>_<sup>)</sup> units of the UA, lending _<sub>Ke</sub><sup>−r</sup>_<sup>(</sup>_<sup>T−t</sup>_<sup>)</sup> and buying the European call. Today this strategy yields a strictly positive cash flow. Upon call maturity, the net position is _<sub>K − S</sub>_(_<sub>T</sub>_) plus the European call value. If the call is out of the money, the position is strictly positive. Otherwise, the exercise of the European call exactly offsets the position. In both cases, the strategy turns out to be an arbitrage. Under the AoA, equation (1.8) is therefore verified.

Finally, equation (1.9) can be simply justified by noticing that the right associated with the European

call is included within the right associated with the American call.□ The last two results yield an important property.

**Proposition 1.13** _When the UA is a spot asset without any dividend, then_

_c_(_t,T,K_) = _C_ (_t,T,K_)_,_

_meaning it is never optimal to exercise the American call before maturity._ **Proof** Combining equations (1.8) and (1.9) and setting _<sub>y</sub>_ \= 0,

_C_ (_t,T,K_) _≥ c_(_t,T,K_)_._

In particular

_C_ (_t,T,K_) _≥ S_(_t_) _− Ke<sup>−r</sup>_<sup>(</sup>_<sup>T−t</sup>_<sup>)</sup>_._

For strictly positive interest rates, this yields

_C_ (_t,T,K_) _\> S_(_t_) _− K._

That is, the American call is always worth more than its intrinsic value. Therefore it should never be exercised before maturity.□

### 1.3.2 Bounds for the put premium

Using similar arguments, we obtain the following results about the European and American put premiums. **Proposition 1.14** _Under the AoA, the following holds_

|     |     |
| --- | --- |
| _P_ (_t,T,K \|S_(_t_) = 0) = _K,_ | (1.10) |
| _P_ (_t,T,K_) _≥_ max(_K − S_(_t_)_,_0)_,_ | (1.11) |
| _P_ (_t,T,K_) _≤ K,_ | (1.12) |
| _p_(_t,T,K_) _≥_ max _Ke−r_(_T−t_) _− S_(_t_)_e−y_(_T−t_)_,_0_,_ | (1.13) |
| _P_ (_t,T,K_) _≥ p_(_t,T,K_)_._ | (1.14) |

The proofs for equations (1.10) to (1.14) are analogous to the ones for equations (1.5) to (1.9). Notice that, in all generality, there is no sufficient condition for the equality between the European put premium and the American put premium. This is due in particular to the fact that the value of the European put may decrease with time to maturity. Another line of interpretation is that the payoff of the call option is unbounded (the UA price can get arbitrarily high). In the absence of dividends, it is therefore always worthwhile to postpone the exercise. By contrast, the strike price is an upper bound for the payoff of the put option. Such upper bound might make it preferable to exercise the put before maturity. The following example illustrates this point.

**Example 1.15** _Consider the American put with strike 25 and 6-month time to maturity, written on an UA worth 1. The risk-free rate is 9%. Immediate exercise of the put yields_ 25 _<sub>−</sub>_ 1 = 24_, which becomes after 6 months of compounding_

241 + 9% \= 25_<sub>.</sub>_08_<sub>.</sub>_

_But whatever the evolution of the UA price, the put option can never be worth more than 25. The put should therefore be exercised now._□

It is also worth noting that in the above properties for European and American options, the current time and maturity date always interact to yield time to maturity _<sub>T−t</sub>_. As exemplified by the wording of the previous example, these options are thus often described in terms of the latter quantity, as _<sub>O</sub>_(_<sub>t,T,K</sub>_) = _O_(0_<sub>,T</sub> − <sub>t,K</sub> |<sub>S</sub>_ \= _<sub>S</sub>_(_<sub>t</sub>_))_<sub>,</sub>O ∈ {<sub>c,C,p,P</sub>}_. For some exotic options with strong path dependence, this relationship does not hold true.

### 1.3.3 Option values before maturity

Using the arbitrage relations in the former section, we can have a better understanding of how option values behave before maturity. For clarity of exposition, we restrict our attention to the UA without any dividend. From equations (3.4) and (3.5), we get (at _<sub>t</sub>_ \= 0, without loss in generality).

_C_ (0_,T,K_) _≥ c_(0_,T,K_) _≥ S_(0) _− Ke<sup>−rT</sup> ._

Thus, when the call is deep out of the money, the speculative value goes to zero. When the call is deep in the money, the speculative value gets close to _<sub>K − Ke</sub><sup>−rT</sup>_ as illustrated by Figure 1.5.

_KB_

(0

,

_T_

)

.

_K_

0

$

_S_(_T_)

Figure 1.5: Value of a call.

The value of the call, be it European or American, goes in the direction shown by the arrows as the risk-free rate, the maturity date, or the UA volatility increase.

As far as put options are concerned, arbitrage relations (3.9) and (3.10) establish that

_P_ (0_,T,K_) _≥ p_(0_,T,K_) _≥ Ke<sup>−rT</sup> − S_(0)_._

Hence Figure 1.6 representing the value of the put premiums before maturity.

_KB_

(0

,

_T_

)

.

_K_

0

$

European

American

_S_(_T_)

Figure 1.6: Value of a put.

Notice that the European put can be worth less than its intrinsic value. This of course can never be the case for the American put because of early exercise. From Figure 1.6 we see it is optimal to exercise the American put when the UA is below the critical level _<sub>A</sub>_.

### 1.3.4 Parity and symmetry relations

##### Put-call parity

The put-call parity, initially presented by Stoll (1969), is an arbitrage relation between the premiums of the European call and put written on the same UA, with same strike and maturity. In all generality, the UA is assumed to generate a continuous dividend at rate _<sub>y</sub>_.

**Proposition 1.16** _(Put-call parity) Under the AoA, the European call and put premiums satisfy_

_c_(0_,T,K_) _− p_(0_,T,K_) = _S_(0)_e<sup>−yT</sup> − Ke<sup>−rT</sup> ._ (1.15)

**Proof** Consider the following arbitrage portfolio: Selling the European call, buying the European put, buying _<sub>e</sub><sup>−yT</sup>_ units of the UA, and borrowing the amount _<sub>Ke</sub><sup>−rT</sup>_ . Upon option maturity, we examine the value of the portfolio depending on which option ends up in the money.

|     |     |     |
| --- | --- | --- |
|     | _S_(_T_) _≤ K_ | _S_(_T_) _\> K_ |
| ~~Short in the call~~ | ~~0~~ | _K − S_~~(~~_T_~~)~~ |
| Long in the put | _K − S_(_T_) | 0   |
| Long in _one_ unit of the UA | _S_(_T_) | _S_(_T_) |
| Paying back the loan | _−K_ | _−K_ |
| Net position | 0   | 0   |

Under the AoA, the initial value of this portfolio must be nil, which ends up the proof.□

The put-call parity can easily be extended to the cases where the UA pays discrete dividends or when the UA is a forward contract. When the UA pays the dividends _<sub>d</sub>_(_<sub>tn</sub>_) at dates _<sub>tn</sub>_, the strategy using a similar arbitrage portfolio entails that

_c_(0_,T,K_) _− p_(0_,T,K_) = _S_(0) _−_ <sup>X</sup>_d_(_t<sub>n</sub>_)_e<sup>−rtn</sup> − Ke<sup>−rT</sup> ._

_n_

When the UA is a forward contract with delivery date _<sub>θ > T</sub>_, the put-call parity becomes

_c_(0_,T,K_) _− p_(0_,T,K_) = (_f_(0_,θ_) _− K_)_e<sup>−rT</sup> ._

The put-call parity essentially means that among the following four assets: The UA, the European call, the European put, and the risk-free asset, one asset is redundant. In other words, a position in any one of these four assets can be synthetically replicated by taking positions in the other three assets.

##### Put-call parity for American options

A comparable put-call parity cannot be established for American options. However, inequality relations hold under the AoA.

**Proposition 1.17** _(Put-call parity for American options) Under the AoA, the American call and put premiums satisfy_

_S_(0)_e<sup>−yT</sup> − K ≤ C_(0_,T,K_) _− P_(0_,T,K_) _≤ S_(0) _− Ke<sup>−rT</sup> ._ (1.16)

**Proof** We start by proving the right-hand side inequality. Consider the following arbitrage portfolio: Buying the American put, selling the American call, buying one unit of the UA, and borrowing the amount

_Ke<sup>−rT</sup>_ . We further commit to not exercising the put before maturity. Two cases must then be examined. Either (a) the call is exercised before maturity, say at time _<sub>τ < T</sub>_: In that case, the value of the portfolio is

_P_(_τ,T,K_) + _S_(_τ_)_e<sup>yτ</sup> − Ke<sup>−r</sup>_<sup>(</sup>_<sup>T−τ</sup>_<sup>)</sup> _−_ (_S_(_τ_) _− K_)

\=_P_(_τ,T,K_) + _S_(_τ_)(_e<sup>yτ</sup> −_ 1) + _K_(1 _− e<sup>−r</sup>_<sup>(</sup>_<sup>T−τ</sup>_<sup>)</sup>) _\>_ 0_._

Or (b) the call is not exercised before maturity: In that case, the value of the portfolio is

|     |     |     |
| --- | --- | --- |
|     | _S_(_T_) _≤ K_ | _S_(_T_) _\> K_ |
| Short in the call | 0   | _K − S_(_T_) |
| Long in the put | _K − S_(_T_) | 0   |
| Long in _<sub>e</sub><sup>yT</sup>_ units of the UA | _e<sup>yT</sup> S_(_T_) | _e<sup>yT</sup> S_(_T_) |
| Paying back the loan | _−K_ | _−K_ |
| Net position | _S_(_T_)_eyT −_ 1 | _S_(_T_)_eyT −_ 1 |

Consequently, the terminal value of the portfolio is positive in all cases. Hence, under the AoA, the initial value of the portfolio must not be strictly positive, that is _<sub>C</sub>_(0_<sub>,T,K</sub>_)_−<sub>P</sub>_(0_<sub>,T,K</sub>_)_−<sub>S</sub>_(0)+_<sub>Ke</sub><sup>−rT</sup> ≤_ 0_<sub>.</sub>_

The left-hand side inequality can be proved in a similar manner.□

In the special case where the UA is a spot asset without any dividends, we have shown that the American call is worth the European call. Hence the put-call parity for American options can be simplified using the put-call parity for European options, which yields

0 _≤ P_(0_,T,K_) _− p_(0_,T,K_) _≤ K_(1 _− e<sup>−rT</sup>_ )_._ (1.17)

Using the first order approximation _<sub>e</sub><sup>−rT</sup> <sub>≈</sub>_ 1 _<sub>− rT</sub>_, the above result implies that an upper bound for the put early exercise premium is _<sub>KrT</sub>_.

##### Put-call symmetry for American options

The following symmetry relation was initially reported in Chesney and Gibson (1995) and McDonald and Schr¨oder (1998)

_C_(_t,T,K |S_(_t_)_,r,y_) = _P_(_t,T,S_(_t_)_|K,y,r_)_._ (1.18)

The intuition for this result goes as follows. An American option can be viewed as an exchange option. The American call offers the right to exchange cash against the UA, while the American put offers the right to exchange the UA against cash. As time passes, the UA appreciates at rate _<sub>y</sub>_ while cash appreciates at rate _<sub>r</sub>_. Hence it is economically equivalent to swap cash against the UA when the interest rate is _<sub>r</sub>_ and the UA has a dividend yield of _<sub>y</sub>_, or to swap the UA against cash when the interest rate is _<sub>y</sub>_ and the UA has a dividend yield of _<sub>r</sub>_.

In practice, the put-call symmetry cannot be used in an arbitrage strategy. This is because among _C_(_<sub>t,T,K</sub> |<sub>S</sub>_(_<sub>t</sub>_)_<sub>,r,y</sub>_) and _<sub>P</sub>_(_<sub>t,T,S</sub>_(_<sub>t</sub>_)_|<sub>K,y,r</sub>_), at least one of these two premiums correspond to an option that does not exist (since the risk-free rate and the UA convenience yield can only take on but one value). However, the put-call symmetry is theoretically very important as it entails that the valuation of the American call and the American put does not require two distinct approaches. If a model can price, say, the American call, then, from the put-call symmetry, a simple change of input values allows to price the American put within the same model. That change of inputs merely consists in swapping _<sub>S</sub>_ and _<sub>K</sub>_, and _<sub>r</sub>_ and _<sub>y</sub>_.

## 1.4 Hedging with derivatives

In this section we describe the main hedging strategies involving forward, futures or options contracts. Hedging consists in reducing the risk associated with a commercial or financial position. We will first examine hedging with forwards or futures. In theory, perfect hedging (i.e., turning the initial risky position into a certainty equivalent) can be achieved with forward or futures contracts unless there is a mismatch between the asset involved in the position to hedge and the UA of the hedging instrument. This mismatch is typically referred to as the basis risk. That basis risk entails some residual uncertainty that can be optimally managed if we specify the hedger’s risk preferences. Next, we will examine hedging with options. Because of the flexibility associated with these hedging instruments, hedging strategies involving options may also include some speculation.

### 1.4.1 Hedging with forwards or futures

##### No basis risk

Consider an agent with a long position of _<sub>x</sub>_ units in asset _<sub>S</sub>_. If that agent can trade in a forward contract written on _<sub>m</sub>_ units of that same asset, then, for any maturity _<sub>T</sub>_, a perfect hedge can be achieved by selling at time 0 a quantity _<sub>h</sub>_ \= _<sub>x/m</sub>_ of forward contracts. The position upon maturity will be

_xS_(_T_) + _h × m_(_f_ (0_,T_) _− S_(_T_)) = _xf_ (0_,T_)_._

In the AoA, the cash and carry relation prevails and the hedged position will be worth _<sub>xSe</sub>_<sup>(</sup>_<sup>r−y</sup>_<sup>)</sup>_<sup>T</sup>_ at time

_T_.

Similarly, an initial short position of _<sub>x</sub>_ units in asset _<sub>S</sub>_ can be hedged by purchasing _<sub>h</sub>_ units of forwards.

The agent’s position upon maturity will be _<sub>−xSe</sub>_<sup>(</sup>_<sup>r−y</sup>_<sup>)</sup>_<sup>T</sup>_ .

Note that even if the interest rate and / or the convenience yield are stochastic, perfect hedging remains feasible with forwards because the forward price _<sub>f</sub>_ (0_<sub>,T</sub>_) is known at time 0.

Suppose now that the agent can trade in a futures contract written on _<sub>m</sub>_ units of asset _<sub>S</sub>_. Hedging becomes more difficult because of all interim payments caused by the marking to market of the futures contract. Specifically, to hedge a long position of _<sub>x</sub>_ units in asset _<sub>S</sub>_, the agent can sell at time 0 a quantity _h_ of futures contracts. On each day _<sub>tn</sub>_ during _<sub>N</sub>_ days (_<sub>t</sub>_<sub>0</sub> \= 0, _<sub>tN</sub>_ \= _<sub>T</sub>_), the agent will receive

_h × m_(_F_ (_t<sub>n−</sub>_<sub>1</sub>_,T_) _− F_ (_t<sub>n</sub>,T_))_._

Capitalizing all interim cash flows until _<sub>T</sub>_ (using compound factors 1_<sub>/B</sub>_ (_<sub>tn,T</sub>_)), the agent will obtain the following position upon maturity

(_T_) + _h × m_ X_<sup>N</sup>_\=1 _F_ (_t<sub>n−</sub>_<sub>1</sub>_B,T_(_t_)_n−,TF_)(_t<sub>n</sub>,T_)_. xS_

_n_

Setting _<sub>h</sub>_ \= _<sub>x/m</sub>_ eliminates the exposure to terminal price risk (_<sub>S</sub>_(_<sub>T</sub>_) or, equivalently, _<sub>F</sub>_ (_<sub>T,T</sub>_)). However, the position upon maturity remains subject to sources of risk that will be difficult to fully hedge away. First, it depends on all interim futures prices _<sub>F</sub>_ (_<sub>tn,T</sub>_) which are affected by UA spot price risk and also possibly by interest rate risk and convenience yield risk. Second, it depends on the discount factors _<sub>B</sub>_ (_<sub>tn,T</sub>_) that represent an additional source of risk if interest rates are stochastic.

##### Basis risk

In practice, the UA of the derivative instrument may not be exactly the same asset that the agent wishes to hedge. This is particularly the case on commodity markets. Commodities differ in quality as well as in delivery location. One example is the Brent / WTI (West Texas Intermediate) spread for crude oil. Brent is deliverable in Rotterdam while WTI is deliverable in Cushing, Oklahoma. This situation entails that the basis will not converge to zero, i.e., _<sub>F</sub>_ (_<sub>T,T</sub>_) _<sub>≈ S</sub>_(_<sub>T</sub>_), thereby harming the quality of the hedge.

In the presence of basis risk, perfect hedge is not feasible. Even the most risk averse hedger must deal with some residual risk. The solution to the hedging problem therefore depends on the hedger’s attitude towards risk. A simple approach is the mean-variance framework where the expected utility of a position Π is

E \[_<sub>U</sub>_ (Π)\] = E \[Π\] _<sub>−</sub>_  Var (Π)_<sub>,</sub>_

where _<sub>α</sub>_ stands for the risk aversion coefficient.

Consider hedging a cash position _<sub>qs</sub>_ in asset _<sub>S</sub>_ with a futures position _<sub>qh</sub>_. The one-period position is

Π = _q<sub>s</sub>_ (_S_(1) _− S_(0)) + _q<sub>h</sub>_ (_F_ (0_,T_) _− F_ (1_,T_))_._

Expressed in terms of gross returns

_<sub>R</sub>_ \= _q<sub>s</sub>S_Π(0) = _<sup>S</sup>_(1)_<sub>S</sub>−_(0)_<sup>S</sup>_(0) + _q<sub>q</sub><sup>h</sup>s F<sub>S</sub>_(0(0)_<sup>,T</sup>_) (_<sup>F</sup>_ (0_,T<sub>F</sub>_)(0_−<sub>,T</sub>F_)(1_<sup>,T</sup>_))

\= _Rs − qh F_ (0(0)_,T_)_Rf_ \= _Rs − hRf,_

_qs S_

where _<sub>Rs</sub>_ and _<sub>Rf</sub>_ denote the spot and the futures one-period returns, and _<sub>h</sub>_ \= _<sup>q</sup><sub>q</sub><sup>h</sup><sub>s</sub> <sup>F</sup><sub>S</sub>_<sup>(0</sup><sub>(0)</sub>_<sup>,T</sup>_<sup>)</sup> denotes the hedge ratio defined as the ratio of futures holdings over cash holdings.

The variance of _<sub>R</sub>_ is

Var (_R_) = _σ<sub>s</sub>_<sup>2</sup> \+ _h_<sup>2</sup>_σ<sub>f</sub>_<sup>2</sup> _−_ 2_hσ<sub>sf</sub>,_

where _<sub>σs</sub>_<sup>2</sup> and _<sub>σf</sub>_<sup>2</sup> denote the variance of the spot and futures returns, respectively, and _<sub>σsf</sub>_ is the covariance between these two returns.

The pure hedging strategy consists in minimizing Var (_<sub>R</sub>_) which leads to

_h__._

_f_

This is the _minimum variance hedge ratio_ which can be estimated from an OLS regression of spot returns on futures returns.

One can measure the effectiveness of the hedge with

\= 1 _−_ min(Var (2 _<sub>R</sub>_))_._

_HE <sub>σ</sub>s_

Since

min(Var (_R_)) = _σ_<sup>2</sup> \+ _h<sup>∗</sup>_<sup>2</sup>_<sub>σ</sub>_<sup>2</sup> _−_ 2_h<sup>∗</sup><sub>σ</sub>_ \= _σ_<sup>2</sup> _− <sup>σ</sup> <sub>,</sub>_

then

_HE_ \= _σ_2_sf_2_σf_2 = _ρ_2_._

_σs_

Thus, the hedge effectiveness can be measured by the squared correlation between spot and futures returns,

i.e., the R<sup>2</sup> of the univariate OLS regression of spot returns on futures returns.

In line with mean-variance preferences, the solution to the hedging problem is rather

maxE \[_R_\] _− <sup>α</sup>_2 Var (_R_)

\= maxE \[_Rs_\] _− h_E \[_Rf_\] _− α_2 _σs_2 + _h_2_σf_2 _−_ 2_hσsf._

Applying the First Order Condition on _<sub>h</sub>_ yields

_h__._

_f f_

The optimal _mean-variance hedge ratio_ thus appears as the minimum variance hedge ratio plus a speculative term. The decision to ”under-” or ”over-” hedge (sometimes referred to as ”active” hedging) will depend on the hedger’s risk aversion _<sub>α</sub>_, the volatility on futures returns _<sub>σf</sub>_, and on the expected futures return E \[_<sub>Rf</sub>_\] or, more simply, on the difference _<sub>F</sub>_ (0_<sub>,T</sub>_) _<sub>−</sub>_ E \[_<sub>F</sub>_ (1_<sub>,T</sub>_)\]. That difference is related to the slope of the term structure of futures prices, as explained below.

##### Backwardation versus contango

In theory, one can wonder whether futures prices are unbiased predictors of future spot prices. A situation where _<sub>F</sub>_ (0_<sub>,T</sub>_) _<sub><</sub>_ E \[_<sub>S</sub>_(_<sub>T</sub>_)\] is referred to as backwardation. In this case, the futures price is a downwardly biased predictor of the future spot price, and the futures price converges to the terminal spot price from below. On many commodity markets, backwardation is deemed normal since the marginal hedger is a producer (not a consumer) and therefore hedges a long position (by selling forward). The producer’s demand for hedging therefore drives the forward price down.

In practice, a market is said to be in backwardation if we observe that _<sub>F</sub>_ (0_<sub>,T</sub>_) _<sub>< S</sub>_ and the term structure of futures prices (the ”futures curve”) is downward sloping. Though backwardation may in theory be a normal situation, it is not observed all the time on all futures markets. The opposite situation, where _<sub>F</sub>_ (0_<sub>,T</sub>_) _<sub>\> S</sub>_ and the futures curve is upward sloping, is known as contango. The simple cash and carry relation (with constant parameters) entails that _<sub>f</sub>_ (0_<sub>,T</sub>_) = _<sub>S</sub>_ exp\[(_<sub>r − y</sub>_)_<sub>T</sub>_\]. Thus, the case of backwardation versus contango critically depends on the difference between the term structures of interest rates and convenience yields.

When it comes to mean-variance hedging, the difference _<sub>F</sub>_ (0_<sub>,T</sub>_) _<sub>−</sub>_ E \[_<sub>F</sub>_ (1_<sub>,T</sub>_)\] is closely related to

_F_ (0_<sub>,T</sub>_) _− <sub>F</sub>_ (0_<sub>,T</sub> −_ 1) (to the extent that _<sub>F</sub>_ (0_<sub>,T</sub> −_ 1) is a good predictor for E \[_<sub>F</sub>_ (1_<sub>,T</sub>_)\]). Thus, in a market in backwardation,

_F_ (0_,T_) _− F_ (0_,T −_ 1) _<_ 0_,_

which reduces the optimal mean-variance hedge ratio, that is, the agent has the incentive to underhedge a long position in the spot asset.

### 1.4.2 Hedging with options

##### Basic strategies

Consider again an agent with a long position of _<sub>x</sub>_ units in asset _<sub>S</sub>_. Instead of hedging that position by selling forwards or futures, the agent can use the put contracts each written on _<sub>m</sub>_ units of _<sub>S</sub>_ and buy _h_ \= _<sub>x/m</sub>_ units of them. The puts, when in the money, will protect the agent’s long position against a decrease in UA price. But if that price moves favorably (i.e., upwards), the puts will be out of the money and the agent will benefit from the initial long position.

Formally, the profit of this position is:

_x_<sup>h</sup>_S_(_T_) _− S_(0)_e<sup>rT</sup>_ <sup>i</sup> \+ _hm_<sup>h</sup>(_K − S_(_T_))<sup>\+</sup> _− pe<sup>rT</sup>_ <sup>i</sup> \= _x_<sup>h</sup>max_{K,S_(_T_)_}−_(_S_(0) + _p_)_e<sup>rT</sup>_ <sup>i</sup>_,_

| Payoff{z } |Initial cost{z }

where _<sub>p</sub>_ is the put premium per unit of _<sub>S</sub>_. Graphically:

A: Profit B: Value at T

K

_S_

(

_T_

)

\-

p

0

$

Underlying

Long put

Protective put

K

_S_

(

_T_

)

p

\-

0

K-p

_e_

_rT_

$

Figure 1.7: Protective put (_<sub>x</sub>_ \= 1).

As opposed to Figures 1.1, 1.3, and 1.4 that report _payoffs_, a _profit_ graph like Panel A of Figure 1.7 further accounts for the cost of setting the position. If the agent already holds the stock, they might sometime disregard the future value of establishing the position in the stock, _<sub>S</sub>_(0)_<sub>e</sub><sup>rT</sup>_ . In that spirit, Panel B of Figure 1.7 reports the value of the position at _<sub>T</sub>_. In both interpretations of the strategy, however, it is clear that premium of the put becomes the (limited) downside of this stategy, and also reduces the upside compare to a naked position in the underlying. This hedging strategy is more flexible than hedging with forwards or futures, since the agent can select the strike price, i.e., the minimum value of the payoff at maturity. The higher _<sub>K</sub>_, the better protection against downside risk, but the more expensive the put option. Conversely, the hedging strategy using a put with a low _<sub>K</sub>_ is more speculative.

Similarly, a short position of _<sub>x</sub>_ units in asset _<sub>S</sub>_ can be hedged by purchasing _<sub>h</sub>_ units of call options, yielding the following profit at time _<sub>T</sub>_:

_−x × S_(_T_) + _h × m_(_S_(_T_) _− K_)<sup>\+</sup> _− ce<sup>rT</sup>_ \= _−x_min(_K,S_(_T_)) _− ce<sup>rT</sup> ._

_x_<sup>h</sup>_S_(0)_e<sup>rT</sup> − S_(_T_)<sup>i</sup> \+ _hm_<sup>h</sup>(_S_(_T_) _− K_)<sup>\+</sup> _− ce<sup>rT</sup>_ <sup>i</sup> \= _x_<sup>h</sup>_−_min_{K,S_(_T_)_}_\+ (_S_(0) _− c_) _e<sup>rT</sup>_ <sup>i</sup>_,_

| Payoff{z } Initial cash flow| {z }

where _<sub>c</sub>_ is the call premium per unit of _<sub>S</sub>_. Figure 1.8 report the profit (per unit) of this strategy.

A: Profit B: Value at T

K

_S_

(

_T_

)

\-

c

0

$

Short underlying

Long call

Protective call

K

_S_

(

_T_

)

\-

c

0

\-

K-c

_e_

_rT_

$

Figure 1.8: Protective call (_<sub>x</sub>_ \= 1).

Again, (minus) the strike price represents the worst payoff for the agent. Hedging with a call option with a smaller _<sub>K</sub>_ reduces the volatility of the final position (i.e., it provides a better hedge), but it increases the hedging cost.

## 1.5 Speculative strategies using options

This section reviews some standard option strategies allowing the investor to achieve specific payoff profiles that can be particularly relevant for speculative motives. These strategies can be classified into two categories: Spreads (which involve options of the same nature, i.e., calls or puts) and combinations (which involve both calls and puts).

### 1.5.1 Spreads

##### Vertical spreads

The bull (bear) spread strategy is adopted by the investor anticipating an increase (decrease) in the UA price. The use of two options limits the potential gains (losses) in case the anticipation turns out to be right (wrong). Both spreads can be constructed with calls only or puts only. The figures below show the profit of a bull spread from calls (Figure 1.9) or from puts (Figure 1.10).

_K_

1

_K_

2

_S_

(

_T_

)

0

$

(

_K_

1

\-

_K_

2

)

(

_c_

1

_c_

2

)

_e_

_rT_

(

_c_

1

_c_

2

)

_e_

_rT_

Long one call

_K_

1

Short one call

_K_

2

Portfolio

_K_

1

_K_

2

_S_

(

_T_

)

0

$

(

_p_

2

_p_

1

)

_e_

_rT_

(

_K_

1

_K_

2

)

+(

_p_

2

_p_

1

)

_e_

_rT_

Figure 1.9: Bull call spread. Figure 1.10: Bull put spread.

The bear spread can be obtained from buying a call with strike _<sub>K</sub>_<sub>2</sub> and selling a call with strike _<sub>K</sub>_<sub>1</sub>, or from buying a put with strike _<sub>K</sub>_<sub>2</sub> and selling a put with strike _<sub>K</sub>_<sub>1</sub>.

##### Horizontal spreads

Horizontal spreads (also known as calendar spreads) involve options with same strike but different maturities. It consists in buying a call with maturity _<sub>T</sub>_<sub>2</sub> and selling a call with maturity _<sub>T</sub>_<sub>1</sub> _<sub>< T</sub>_<sub>2</sub>. A similar strategy can be obtained using puts. An investor buying a calendar spread expects the UA price to exhibit little variations within _<sub>T</sub>_<sub>1</sub>, and then to increase between _<sub>T</sub>_<sub>1</sub> and _<sub>T</sub>_<sub>2</sub>. Indeed, if the UA price stays around the current level at date _<sub>T</sub>_<sub>1</sub>, the short call expires worthless, while the long call will get in the money if the UA price increases afterwards. Figure 1.11 shows the value at date _<sub>T</sub>_<sub>1</sub> of a horizontal spread.

K

_S_

(

_T_

)

0

$

Short one call

_T_

1

Long one call

_T_

2

Value of the

_T_

2

call at

_T_

1

Value of the portfolio at

_T_

1

Figure 1.11: Horizontal spread.

The horizontal spread can be more or less directional depending on the chosen strike. When the options are out of, at, or in the money, the horizontal spread is said to be bullish, neutral or bearish.

The reverse horizontal (calendar) spread consists in buying the short maturity option and selling the long maturity option. An investor using a reverse calendar spread expects the UA price to strongly increase or decrease within _<sub>T</sub>_<sub>1</sub>, and then not to decrease (in case of puts) between _<sub>T</sub>_<sub>1</sub> and _<sub>T</sub>_<sub>2</sub> so that the short option with long maturity expires out of the money. Figure 1.12 shows the time-_<sub>T</sub>_<sub>1</sub> value of a reverse horizontal spread made out of puts.

K

_S_

(

_T_

)

0

$

Long one put

_T_

1

Short one put

_T_

2

Value of the

_T_

2

put at

_T_

1

Portfolio

Figure 1.12: Reverse horizontal spread.

##### Diagonal spreads

A diagonal spread consists in buying an option and selling another one of same nature, but with different strikes and maturities. The payoff profile resembles that of the horizontal spread except that the ”spike” of the spread is wider due to the two different strikes. Therefore the diagonal and horizontal spreads reflect similar anticipations, but the diagonal spread is a more prudent strategy as the UA price interval yielding a gain is larger. By contrast, the reverse diagonal spread is a more speculative strategy than the reverse horizontal spread.

### 1.5.2 Combinations

This subsection reviews some classic combinations. The list is, however, not exhaustive since, as shown below, any arbitrary payoff profile can be generated by an adequate combination of options.

##### Straddle

The long position in the call and the put with same strike and maturity is the long straddle. Such a position will benefit from a high volatility of the UA price. Conversely, the short straddle consists in selling the call and the put with same strike and maturity. This strategy is essentially betting on the stagnation of the UA price around the strike price. The figures below show the profits of a long straddle (Figure 1.13) or a short straddle (Figure 1.14).

K

_S_

(

_T_

)

0

$

Long ATM call

Long ATM put

Portfolio

Figure 1.13: Long straddle.

K

_S_

(

_T_

)

0

$

Short ATM call

Short ATM put

Portfolio

Figure 1.14: Short straddle.

##### Strangles

Strangle strategies involve calls and puts with same maturity but different strikes. The figures below show the profits generated by a long strangle (Figure 1.15) or a short strangle (Figure 1.15).

K_1

K_2

_S_

(

_T_

)

0

$

Long

_K_

1

put

Long

_K_

2

call

Portfolio

K_1

K_2

_S_

(

_T_

)

0

$

Short

_K_

1

put

Short

_K_

2

call

Portfolio

Figure 1.15: Long strangle. Figure 1.16: Short strangle.

The long strangle appears like a more aggressive strategy than the long straddle. By contrast, the short strangle is a more conservative strategy than the short straddle.

### 1.5.3 Butterflies, condors and other profiles

The butterfly strategy aims at benefitting from a local anticipation with limited losses. It can be implemented with calls or puts. For instance, the investor can buy one calls with strike _<sub>K</sub>_<sub>1</sub> and one call with strike _<sub>K</sub>_<sub>3</sub>, and sell two calls with strike _<sub>K</sub>_<sub>2</sub> with _<sub>K</sub>_<sub>1</sub> _<sub>< K</sub>_<sub>2</sub> _<sub>< K</sub>_<sub>3</sub>. By adding a fourth strike, one stretches the “wings” of the butterfly to obtain a condor. The investor buys the calls with extreme strikes _<sub>K</sub>_<sub>1</sub> and

_K_<sub>4</sub>, and sells the calls with intermediate strikes _<sub>K</sub>_<sub>2</sub> and _<sub>K</sub>_<sub>3</sub>. The figures below illustrate the butterfly (Figure 1.17) and the condor (Figure 1.18) strategies.

_K_

1

_K_

2

_K_

3

_S_

(

_T_

)

0

$

Long one call

_K_

1

Short two calls

_K_

2

Short one call

_K_

3

Portfolio

_K_

1

_K_

2

_K_

3

_K_

4

_S_

(

_T_

)

0

$

Long one

_K_

1

call

Short one

_K_

2

call

Short one

_K_

3

call

Long one

_K_

4

call

Portfolio

Figure 1.17: Butterfly. Figure 1.18: Condor.

Butterflies and condors are based on anticipations that are similar to those motivating short straddles or short strangles. The main difference is that butterflies and condors are more prudent given that the potential losses are capped. Of course, it is also possible to short a butterfly or a condor, which corresponds to a bet on the UA price volatility with capped potential gains.

Finally, it should be noted that any payoff profile that is piecewise linear can be obtained by an appropriate combination of options. For example, the payoff profile illustrated in Figure 1.19 can be obtained using calls or puts.

- Using calls, the positions are determined by scanning the profile from left to right. The profile begins with buying the call with strike _<sub>K</sub>_<sub>1</sub>. Then the slope of the profile shifts from +1 to _<sub>−</sub>_1\. One must therefore sell two calls with strike _<sub>K</sub>_<sub>2</sub>. Then the slope goes from _<sub>−</sub>_1 to +2, which implies one must buy three calls with strike _<sub>K</sub>_<sub>3</sub>. Finally, the slope decreases to _<sub>−</sub>_1, which requires the sell of three calls with strike _<sub>K</sub>_<sub>4</sub>.
- Using puts, the positions are determined by scanning the profile from right to left. The slope begins at _<sub>−</sub>_1\. One must therefore short sell one unit of the UA. Then the slope shifts from _<sub>−</sub>_1 to +2. One must therefore sell three puts with strike _<sub>K</sub>_<sub>4</sub>. The slope then decreases to _<sub>−</sub>_1, which means that three puts with strike _<sub>K</sub>_<sub>3</sub> must be bought. Finally, the sell of two puts with strike _<sub>K</sub>_<sub>2</sub> and the purchase of one put with strike _<sub>K</sub>_<sub>1</sub> complete the profile.

_K_

1

_K_

2

_K_

3

_K_

4

_S_

(

_T_

)

0

$

Slope = +1

Slope = -1

Slope = +2

Slope = -1

Figure 1.19: Piecewise linear payoff.

In sum, the desired payoff profile can be obtained with the following two strategies.

Using calls Using puts

|     |     |     |
| --- | --- | --- |
| ~~Strike~~ _K_<sub>1</sub> | ~~Buy one~~ | ~~Buy one~~ |
| Strike _K_<sub>2</sub> | Sell two | Sell two |
| Strike _K_<sub>3</sub> | Buy three | Buy three |
| Strike _K_<sub>4</sub> | Sell three | Sell three |
| UA  | Nothing | Sell one |

Notice that these two strategies are equivalent because of the put-call parity.

## 1.6 Problem set

#### Exercise 1.1

Assuming the basis is defined as the forward price minus the spot price, give an example of an asset typically associated with a positive basis (i.e., contango).

#### Exercise 1.2

An investment strategy, known as the _covered call_, consists in selling a call option while being long in the UA. What option position is that strategy equivalent to?

#### Exercise 1.3

The 3-month forward price of one pound of molybdenum is $12. The cost of carry for molybdenum is assumed to be 4%. The continuously compounded 3-month risk-free rate is 6%. On the spot market, one pound of molybdenum is worth $11.9. Construct an arbitrage strategy.

#### Exercise 1.4

The 3-month and 6-month futures prices of a pound of copper are $2.76 and $2.78, respectively. The 3-month and 6-month risk-free rates are 2% and 3%, respectively. What is the convenience yield for copper assuming it is a constant? What is the spot price of copper?

#### Exercise 1.5

You observe the following bid-ask quotes for European options written on the same UA and maturing in 50 days:

~~Option Strike Bid Ask~~

Call 100 13.4 13.9

Call 120 3.1 3.3

Put 100 1.4 1.5

Put 120 9.7 10.1

The UA is currently quoted at $112 and the risk-free rate is 5%. No dividends are expected until the options maturity. Construct an arbitrage strategy involving only options.

#### Exercise 1.6

A Canadian company will receive a payment of 100,000 USD in one month. The treasurer is hedging with a zero premium tunnel made of a one-month put on the USD/CAD exchange rate with strike 1 USD = 1.29 CAD and a one-month call on the USD/CAD exchange rate with strike 1 USD = 1.32 CAD.

1.  What will be the company’s net position in CAD in one month if the USD/CAD exchange rate is 1.28, 1.3, or 1.33?
2.  Give a lower and an upper bound for the one-month USD/CAD forward exchange rate in the absence of arbitrage.

#### Exercise 1.7

The UA with current price _<sub>S</sub>_(0) will pay a dividend _<sub>d</sub>_ at time _<sub>t</sub>_ (0 _<sub>< t < T</sub>_). Show that

_P_(0_,T,K_) _≥_ max(_P_<sub>1</sub>;_P_<sub>2</sub>)_,_

with

_P_<sub>1</sub> \= max(0;_<sub>K</sub> − <sub>S</sub>_(0))_<sub>,</sub>_

_P_<sub>2</sub> \= max0;(_K_ \+ _d_)_e<sup>−rt</sup> − S_(0)_,_

where _<sub>r</sub>_ denotes the risk-free rate.

#### Exercise 1.8

The European call and put, with strike _<sub>K</sub>_ \= 102, and maturity _<sub>T</sub>_ \= 3 months, written on stock _<sub>S</sub>_ are quoted

_c_ \= 5_._64_, p_ \= 6_._37_._

The stock is currently worth _<sub>S</sub>_(0) = 100 and no dividend is expected within three months.

1.  What is the value of the American call with same characteristics?
2.  What upper and lower bounds can you suggest for the American put with same characteristics ?

#### Exercise 1.9

Consider the stock _<sub>S</sub>_ paying a dividend _<sub>D</sub>_ at time _<sub>θ</sub>_. Let _<sub>θ</sub><sup>−</sup>_ and _<sub>θ</sub>_<sup>\+</sup> denote the moments right before and after the dividend is paid out. Suppose that the stock instantly drops by the amount _<sub>D</sub>_ following the payment of the dividend, that is,

_S θ_\+ = _S θ−_ _− D._

Consider a derivative _<sub>g</sub>_ written on _<sub>S</sub>_. Show that, under the AoA, the price of the derivative remains continuous after the dividend payment, that is,

_g θ_\+ = _g θ−._

#### Exercise 1.10

The stock of a listed oil company is worth 40. You observe the following quotes for 3-month options:

##### ~~Option Strike Quote Option Strike Quote~~

Call 35 5.8 Put 35 0.5

Call 40 2.5 Put 40 2.2

Call 45 0.9 Put 45 5.5

No dividend is expected within the next three months. The company will soon announce the results from oil exploration on some of its wells. You anticipate that the results will be either extremely positive or totally disappointing. Describe the speculative strategy using options you wish to implement.

#### Exercise 1.11

A producer wants to hedge the sale of 200,000 pounds of copper. The historical variance of copper spot prices is 30%. The historical volatility of copper futures prices is 40%. The covariance between these two returns is 10%.

1.  How many futures should the producer buy or sell to minimize the variance of the position (the copper futures contract is written on 25,000 pounds)?
2.  What is the hedge effectiveness?
3.  In a mean-variance framework, would the producer buy or sell more or fewer futures contracts if copper is in contango?

#### Exercise 1.12

A speculator would like to have the following position in the UA in 3 months:

##### ~~Price range Slope of position Price range Slope of position~~

0 _≤ S_(_T_) _< A_ +1 _B ≤ S_(_T_) _< C_ +0_._5 _A ≤ S_(_T_) _< B_ 0 _C ≤ S_(_T_) _−_1

Determine the combination of 3-month call options achieving the desired position.

## 1.7 Solutions

#### Solution 1.1

The basis reflects the trade-off between the benefits from holding the asset (including dividends, coupon payments, convenience yield) and the benefits from postponing its acquisition (including cost of carry, storage cost). The basis is likely to be positive (contango) for an asset that is expensive to hold. One example is a precious metal like gold.

#### Solution 1.2

The covered call yields the terminal payoff

_S_(_T_) _−_ max(0_,S_(_T_) _− K_) = _K −_ max(0_,K − S_(_T_))_._

It is equivalent to shorting a put.

#### Solution 1.3

According to the cash and carry relation, the theoretical forward price is

11_<sub>.</sub>_9exp(0_<sub>.</sub>_06 _<sub>−</sub>_ 0_<sub>.</sub>_04) 12<sup>3</sup> \= 11_<sub>.</sub>_96 _<sub><</sub>_ 12_<sub>.</sub>_

The arbitrage therefore consists in selling the forward, i.e., it is a cash and carry arbitrage.

#### Solution 1.4

The cash and carry relations applied to the 3- and 6-month horizons yield

2_._76 = _S_(0)exp(0_._02 _− <sub>y</sub>_) 12<sup>3</sup> _<sub>,</sub>_

2_._78 = _S_(0)exp(0_._03 _− <sub>y</sub>_) 12<sup>6</sup> _<sub>,</sub>_

where _<sub>S</sub>_ is the spot price and _<sub>y</sub>_ is the convenience yield. Taking the ratio of the two equations

_y_ \= 0_._03 _−_ 0_._02 _−_ ln <sup>2</sup>2_<sup>.</sup><sub>.</sub>_<sup>78</sup>76 \= 1_._11%_,_

and

_S_(0) = 2_<sub>.</sub>_754_<sub>.</sub>_

#### Solution 1.5

Arbitrage strategies involving options only are referred to as _boxes_. They benefit from lower transaction costs and easier timing. Consider the following strategy:

. buy call 100 and put 120, . sell call 120 and put 100,

. borrow 20_<sub>e</sub><sup>−</sup>_<sup>0</sup>_<sup>.</sup>_<sup>05</sup> = 19_<sub>.</sub>_863.

The strategy is worth zero upon maturity. Today it is worth the arbitrage profit

_−_13_<sub>.</sub>_9 _−_ 10_<sub>.</sub>_1 + 3_<sub>.</sub>_1 + 1_<sub>.</sub>_4 + 19_<sub>.</sub>_86 = 0_<sub>.</sub>_36_<sub>.</sub>_

#### Solution 1.6

1.  If the exchange rate is 1.28, 1.3 or 1.33, the net position will be 129,000 CAD, 130,000 CAD or 132,000 CAD, respectively.
2.  In the AoA, the forward exchange rate should lie within 1.29 and 1.32.

#### Solution 1.7

The value _<sub>P</sub>_<sub>1</sub> corresponds to what the put option holder can obtain with immediate exercise. The value _P_<sub>2</sub> corresponds to what the put option holder can get from exercising right after date _<sub>t</sub>_. Indeed, assuming the stock price drops by an amount _<sub>d</sub>_ at time _<sub>t</sub>_, the exercise of the put yields

max(0_,K −_ (_S_(_t_) _− d_))_,_

which is worth today _<sub>P</sub>_<sub>2</sub>. Since there might be more profitable exercise dates other than 0 or _<sub>t</sub>_, the American put premium must be greater than max(_<sub>P</sub>_<sub>1</sub>_<sub>,P</sub>_<sub>2</sub>).

#### Solution 1.8

1.  In the absence of dividends, the American call is worth the European call, that is, 5.64.
2.  In the AoA, we have the following bounds for the American option premiums

_S_(0) _− K ≤ C_(0_,T,K_) _− P_(0_,T,K_) _≤ S_(0) _− Ke<sup>−rT</sup> ._

Since _<sub>C</sub>_(0_<sub>,T,K</sub>_) = _<sub>c</sub>_(0_<sub>,T,K</sub>_), we obtain (using put-call parity)

_p_(0_,T,K_) _≤ P_(0_,T,K_) _≤ c_(0_,T,K_) _− S_(0) + _K,_

hence

6_._37 _≤ P_(0_,T,K_) _≤_ 7_._64_._

#### Solution 1.9

As opposed to the shareholders, the buyer of the option is not entitled to dividends. Suppose for instance that the market anticipates that _<sub>g θ</sub>_<sup>\+</sup> \= _<sub>g</sub>_ (_<sub>θ</sub><sup>−</sup>_) _<sub>− ε</sub>_. Then an arbitrage strategy consists in selling the option just before _<sub>θ</sub>_ and buying it right afterwards. That strategy induces an immediate arbitrage profit of _<sub>ε</sub>_ since there is no dividend claim against the option trader.

#### Solution 1.10

The anticipation is that the UA price will either increase or decrease substantially. A possible strategy taking advantage of that anticipation is buying an ATM straddle, i.e., buy the call 40 and the put 40 (cost is 4.7). A less expensive, less speculative strategy would be a butterfly: buy the call 40 and the put 40 and sell the put 35 and the call 45 (cost is 3.3). An even less expensive strategy would be the following strangle: buy the put 35 and buy the call 45 (cost is 1.4).

#### Solution 1.11

1.  The producer should sell  _<sub>×</sub>_  = 5 contracts.
2.  The hedge effectiveness is <sub>0</sub>_<sub>.</sub>_<sub>3</sub><sup>0</sup><sub>2</sub>_<sup>.</sup>_<sup>1</sup><sub>0</sub><sup>2</sup>_<sub>.</sub>_<sub>4</sub>2 = 69%.
3.  In contango, the producer will sell more contracts (overhedge) to hedge the long position in copper.

#### Solution 1.12

The speculator first needs to get long in one unit of the UA to obtain the initial slope of +1. Then sell one call with strike _<sub>A</sub>_, buy one half call with strike _<sub>B</sub>_, and sell one and a half call with strike _<sub>C</sub>_.

38 _Derivatives, by Dorion and Fran¸cois, Sunday 24<sup>th</sup> August, 2025_

**Bibliography**

Amin K. (1993). Jump Diffusion Option Valuation in Discrete Time. _Journal of Finance_, _58_, 1833–1863.

Amin K., & Ng V. (1993). _ARCH Processes and Option Valuation_. working paper, University of Michigan.

Anderluh J., & van der Weide H. (2004). Parisian Options – The Implied Barrier Concept. In M. Bubak, G. D. van Albada, P. M. A. Sloot, & J. Dongarra (Eds.), _Computational science - iccs 2004_ (pp. 851– 858). Springer Berlin Heidelberg.

Angus J. (1999). A Note on Pricing Asian Derivatives with Continuous Geometric Averaging. _Journal of Futures Markets_, _19_, 845–858.

Babbs S. (2000). Binomial Valuation of Lookback Options. _Journal of Economic Dynamics and Control_, _24_, 1499–1525.

Barone-Adesi G., & Whaley R. (1986). The Valuation of American Call Options and the Expected ExDividend Stock Price Decline. _Journal of Financial Economics_, _17_, 91–111.

Barone-Adesi G., & Whaley R. (1987). Efficient Analytic Approximation of American Option Values. _Journal of Finance_, _42_, 301–320.

Barraquand J., & Martineau D. (1995). Numerical Valuation of High Dimensional Multivariate American Securities. _Journal of Financial and Quantitative Analysis_, _30_, 383–405.

Basu S., & Hull J. (2021). _Options, Futures and Other Derivatives_. Pearson.

Bates D. (1996). Jumps and Stochastic Volatility: Exchange Rate Processes Implicit in Deustche Mark Options. _Review of Financial Studies_, _9_, 69–107.

Bates D. (2000). Post-’87 Crash Fears in the S&P 500 Futures Option Market. _Journal of Econometrics_, _94_(1/2), 181–238.

Beckers S. (1980). The Constant Elasticity of Variance Model and its Implications for Option Pricing. _Journal of Finance_, _35_, 661–673.

Bergman Y., Grundy B., & Wiener Z. (1996). General Properties of Option Prices. _Journal of Finance_, _51_, 1573–1610.

Bernard C., & Boyle P. (2011). Monte Carlo Methods for Pricing Discrete Parisian Options. _European Journal of Finance_, _17_, 169–196.

Bjerksund P., & Stensland S. (2014). Closed Form Spread Option Valuation. _Quantitative Finance_, _14_, 1785–1794.

Black F. (1976). The Pricing of Commodity Contracts. _Journal of Financial Economics_, _3_, 167–179.

Black F., & Scholes M. (1973). The Pricing of Options and Corporate Liabilities. _Journal of Political Economy_, _81_, 637–654.

39

Bollerslev T. (1986). Generalized Autoregressive Conditional Heteroscedasticity. _Journal of Econometrics_, _31_, 307–327.

Bollerslev T., Chou R., & Kroner K. (1992). Arch Modelling in Finance: A Review of the Theory and Empirical Evidence. _Journal of Econometrics_, _51_, 5–59.

Bossaerts P., & Hillion P. (1997). Local Parametric Analysis of Hedging in Discrete Time. _Journal of Econometrics_, _81_, 243–272.

Boyle P. (1977). Options: A Monte Carlo Approach. _Journal of Financial Economics_, _4_, 323–338.

Boyle P. (1986). Option Valuation Using a Three-jump Process. _International Options Journal_, _3_, 7–12.

Boyle P. (1988). A Lattice Framework for Option Pricing with Two State Variables. _Journal of Financial and Quantitative Analysis_, _23_, 1–12.

Boyle P., & Emanuel D. (1980). Discretely Adjusted Option Hedges. _Journal of Financial Economics_, _8_, 259–282.

Boyle P., & Vorst T. (1992). Option Replication in Discrete Time with Transaction Costs. _Journal of Finance_, _47_, 271–293.

Breeden M., & Litzenberger R. (1978). Prices of State Contingent Claims Implicit in Option Prices. _Journal of Business_, _51_, 621–651.

Brennan M., & Schwartz E. (1978). Finite Difference Methods and Jump Processes Arising in the Pricing of Contingent Claims: A Synthesis. _Journal of Financial and Quantitative Analysis_, _13_, 462–474.

Broadie M., & Detemple J. (1996). American Option Valuation: New Bounds, Approximations, and a Comparison of Existing Methods. _Review of Financial Studies_, _9_, 1211–1250.

Broadie M., & Glasserman P. (1997). Pricing American-Style Securities Using Simulation. _Journal of Economic Dynamics and Control_, _21_, 1323–1352.

Broadie M., & Glasserman P. (1998). Simulation for Option Pricing and Risk Management. _Risk Management and Analysis_, _1_, 173–207.

Broadie M., Glasserman P., & Kou S. (1997). A Continuity Correction for Discrete Barrier Options. _Mathematical Finance_, _7_, 325–348.

Broadie M., & Kaya O. (2006). Exact Simulation of Stochastic Volatility and Other Affine Jump Diffusion¨ Processes. _Operations Research_, _54_, 217–231.

Carmona R., & Durrleman V. (2003). Pricing and Hedging Spread Options. _SIAM Review_, _45_, 627–685.

Carr P., Jarrow R., & Myneni R. (1992). Alternative Characterizations of American Puts. _Mathematical Finance_, _2_, 87–106.

Carri\`ere J. (1996). Valuation of Early-Exercise Price of Options Using Simulations and Nonparametric Regression. _Insurance: Mathematics and Economics_, _19_, 19–30.

Cheang G., & Chiarella C. (2012). _A Modern View on Merton’s Jump-Diffusion Model_. Stochastic Processes, Finance; Control: A Festschrift in Honor of Robert J Elliott.

Chesney M., & Gibson R. (1995). State Space Symmetry and Two-Factor Option Pricing Models. _Advances in Futures and Options Research_, _8_, 85–112.

Chesney M., Jeanblanc M., & Yor M. (1997). Brownian Excursions and Parisian Barrier Options. _Advances in Applied Probabilities_, _29_, 165–184.

Chesney M., & Lefoll J. (1996). Predicting Premature Exercise of an American Put on Stocks: Theory and Empirical Evidence. _European Journal of Finance_, _2_, 21–39.

Cheuk T., & Vorst T. (1997). Currency Lookback Options and Observation Frequency: A Binomial Approach. _Journal of International Money and Finance_, _16_, 173–187.

Christoffersen P., Dorion C., Jacobs K., & Wang Y. (2010). Volatility Components, Affine Restrictions and Non-Normal Innovations. _Journal of Business and Economic Statistics_, _28_, 483–502.

Christoffersen P., & Jacobs K. (2004). Which GARCH Option Model for Valuation? _Management Science_, _50_, 1204–1221.

Cl´ement E., Lamberton D., & Protter P. (2002). An Analysis of a Least Squares Regression Algorithm for American Option Pricing. _Finance and Stochastics_, _6_, 449–471.

Clewlow L., & Carverhill A. (1994). On the Simulation of Contingent Claims. _Journal of Derivatives_, _2_,

66–74.

Cont R., & Tankov P. (2004). _Financial Modelling with Jump Processes_. Chapman; Hall/CRC.

Conze A., & Viswanathan M. (1991a). European Path Dependent Options: The Case of Geometric Averages. _Finance_, _12_(1), 7–22.

Conze A., & Viswanathan M. (1991b). Path Dependent Options: The Case of Lookback Options. _Journal of Finance_, _46_, 1893–1907.

Cox J. (1996). The Constant Elasticity of Variance Option Pricing Model. _Journal of Portfolio Management_, 15–17.

Cox J., Ingersoll J., & Ross S. (1981). The Relation Between Forward Prices and Futures Prices. _Journal of Financial Economics_, _9_, 321–346.

Cox J., & Ross S. (1976). The Valuation of Options for Alternative Stochastic Processes. _Journal of Financial Economics_, _3_, 145–166.

Cox J., Ross S., & Rubinstein M. (1979). Option Pricing: A Simplified Approach. _Journal of Financial Economics_, _7_, 229–263.

Davis M., Panas V., & Zariphopoulou T. (1993). European Option Pricing with Transaction Costs. _SIAM Journal of Control and Optimization_, _31_, 470–493.

Dewynne J., & Wilmott P. (1995). Asian Options as Linear Complementarity Problems: Analysis and Finite-Difference Solutions. _Advances in Futures and Options Research_, _8_, 145–177.

Ding Z., Granger C., & Engle R. (1993). A Long Memory Property of Stock Market Returns and a New Model. _Journal of Empirical Finance_, _1_, 83–106.

Dragulescu A., & Yakovenko V. (2002). Probability Distribution of Returns in the Heston Model with Stochastic Volatility. _Quantitative Finance_, _2_, 443–453.

Duan J. (1995). The Garch Option Pricing Model. _Mathematical Finance_, _5_, 13–32.

Duan J., Gauthier G., Sasseville C., & Simonato J.-G. (2004). _Approximating the GJR-GARCH and EGARCH Option Pricing Models Analytically_. working paper, HEC Montr´eal.

Duan J., & Simonato J.-G. (1998). Empirical Martingale Simulation for Asset Prices. _Management Science_, _44_, 1218–1233.

Engle R., & Ng V. (1993). Measuring and Testing the Impact of News on Volatility. _Journal of Finance_, _48_, 1749–1778.

Fama E. (1965). The Behavior of Stock Market Prices. _Journal of Business_, _38_, 34–105.

Fama E. (1970). Efficient Capital Markets: A Review of Theory and Empirical Work. _Journal of Finance_, _25_, 383–417.

Figlewski S., & Gao B. (1999). The Adaptive Mesh Model: A New Approach to Efficient Option Pricing. _Journal of Financial Economics_, _53_, 313–351.

French K. (1980). Stock Returns and the Weekend Effect. _Journal of Financial Economics_, _8_, 55–69.

Fusai G., & Tagliani A. (2001). Pricing of Occupation Time Derivatives: Continuous and Discrete Monitoring. _Journal of Computational Finance_, _5_, 1–37.

Geske R. (1977). The Valuation of Corporate Liabilities as Compound Options. _Journal of Financial and Quantitative Analysis_, _12_, 541–552.

Geske R. (1979). The Valuation of Compound Options. _Journal of Financial Economics_, _7_, 63–81.

Gesser V., & Poncet P. (1997). Volatility Patterns: Theory and Evidence from the Dollar-Mark Option Market. _Journal of Derivatives_, _5_, 46–61.

Glasserman P. (2004). _Monte Carlo Methods in Financial Engineering_. Springer.

Glosten L., Jagannathan R., & Runkle D. (1993). On the Relationship between the Expected Value and the Volatility of the Nominal Excess Return on Stocks. _Journal of Finance_, _48_, 1779–1801.

Goldman B., Sosin H., & Gatto M. (1979). Path Dependent Options: Buy at the Low, Sell at the High. _Journal of Finance_, _34_, 1111–1127.

Haber R., Sch¨onbucher P., & Wilmott P. (1999). Pricing Parisian Options. _Journal of Derivatives_, _6_, 71–79.

Hagan P., Kumar D., Lesniewski A., & Woodward D. (2002). Managing smile risk. _Wilmott Magazine_, _1_, 84–108.

Harrison M., & Kreps D. (1979). Martingales and Arbitrage in Multiperiod Securities Markets. _Journal of Economic Theory_, _20_, 381–408.

Harrison M., & Pliska S. (1981). Martingales and Stochastic Integrals in the Theory of Continuous Trading. _Stochastic Processes and their Applications_, _11_, 215–260.

Hauser S., & Lauterbach B. (1996). Tests of Warrant Pricing Models: The Trading Profits Perspective. _Journal of Derivatives_, _4_(2), 71–79.

Henrotte P. (1993). _Transaction Costs and Duplication Strategies_. Working Paper, HEC Paris.

Hentschel L. (1995). All in the Family: Nesting Symmetric and Asymmetric GARCH Models. _Journal of Financial Economics_, _39_, 71–104.

Heston S. (1993). A Closed Form Solution for Options with Stochastic Volatility with Applications to Bonds and Currency Options. _Review of Financial Studies_, _6_, 327–343.

Heston S. (1997). _A Simple New Formula for Options with Stochastic Volatility_. Working Paper, Washington University.

Heston S., & Nandi S. (2000). A Closed-form GARCH Option Pricing Model. _Review of Financial Studies_, _13_, 585–626.

Hodges S., & Neuberger A. (1989). Optimal Replication of Contingent Claims under Transaction Costs. _Review of Futures Markets_, _8_, 222–239.

Hoggard T., Whalley E., & Wilmott P. (1994). Hedging Option Portfolios in the Presence of Transaction Costs. _Advances in Futures and Options Research_, _7_, 21–35.

Hsieh K., & Ritchken P. (2005). An Empirical Comparison of GARCH Option Pricing Models. _Review of Derivatives Research_, _8_, 129–150. https://doi.org/10.1007/s11147-006-9001-3

Huang J., Subrahmanyam M., & Yu G. (1996). Pricing and Hedging American Options: A Recursive Integration Method. _Review of Financial Studies_, _9_, 277–300.

Hugonnier J. (1999). The Feynman-Kac Formula and Pricing Occupation-Time Derivatives. _International Journal of Theoretical and Applied Finance_, _2_, 153–178.

Hui C. H., Lo C., & Yuen P. (2000). Constant Elasticity of Variance Option Pricing Model with TimeDependent Parameters. _International Journal of Theoretical and Applied Finance_, _3_, 661–674.

Hull J., & White A. (1987). The Pricing of Options on Assets with Stochastic Volatilities. _Journal of Finance_, _42_, 281–300.

Hull J., & White A. (1988). The Use of the Control Variate Technique in Option Pricing. _Journal of Financial and Quantitative Analysis_, _23_(3), 237–251.

Hull J., & White A. (1990a). Pricing Interest Rate Derivative Securities. _Review of Financial Studies_, _3_(4), 573–592.

Hull J., & White A. (1990b). Valuing Derivative Securities Using the Finite Difference Method. _Journal of Financial and Quantitative Analysis_, _25_(1), 87–100.

Ib´an˜ez A., & Zapatero F. (2004). Monte Carlo Valuation of American Options through Computation of the Optimal Exercise Frontier. _Journal of Financial and Quantitative Analysis_, _39_, 253–275. https://doi.org/10.1017/S0022109000003069

Itˆo K. (1944). Stochastic integral. _Proceedings of the Imperial Academy_, _20_(8), 519–524. [https://doi.org/](https://doi.org/10.3792/pia/1195572786)

[10.3792/pia/1195572786](https://doi.org/10.3792/pia/1195572786)

Jacka S. (1991). Optimal Stopping and the American Put. _Mathematical Finance_, _1_, 1–14.

Jagannathan R. (1984). Call Options and the Risk of Underlying Securities. _Journal of Financial Economics_, _13_, 425–434.

Jamshidian F. (1992). An Analysis of American Options. _Review of Futures Markets_, _11_, 72–82.

Jarrow R., & Oldfield G. (1981). Forward Contracts and Futures Contracts. _Journal of Financial Economics_, _9_, 373–382.

Jarrow R., & Rudd A. (1983). _Option Pricing_. R. Irwin, Homewood.

Ju N. (1998). Pricing an American Option by Approximating Its Early Exercise Boundary as a Multipiece Exponential Function. _Review of Financial Studies_, _11_, 627–646.

Kahl C., & J¨ackel P. (2006). Fast Strong Approximation Monte Carlo Schemes for Stochastic Volatility Models. _Quantitative Finance_, _6_, 513–536.

Karatzas I., & Shreve S. E. (1991). _Brownian Motion and Stochastic Calculus_ (Second). Springer-Verlag.

Kemna A., & Vorst A. (1990). A Pricing Method for Options Based on Average Asset Values. _Journal of Banking and Finance_, _14_, 113–129.

Kim I. (1990). The Analytical Valuation of American Options. _Review of Financial Studies_, _3_, 547–572.

Kirk E. (1995). Correlation in the Energy Markets. In _Managing energy price risk_ (pp. 71–78). Risk Publications; Enron.

Kou S. (2002). A Jump-Diffusion Model for Option Pricing. _Management Science_, _48_, 1086–1101.

Leisen D., & Reimer M. (1996). Binomial Models for Option Valuation: Examining and Improving Convergence. _Applied Mathematical Finance_, _3_, 319–346.

Leland H. (1985). Option Pricing and Replication with Transaction Costs. _Journal of Finance_, _40_, 1283– 1301.

Longstaff F., & Schwartz E. (2001). Valuing American Options by Simulation: A Simple Least-Squares Approach. _Review of Financial Studies_, _14_, 113–147.

Lord R., Koekkoek R., & Dijk D. (2010). A Comparison of Biased Simulation Schemes for Stochastic Volatility Models. _Quantitative Finance_, _10_, 177–194.

MacMillan L. (1986). Analytic Approximation for the American Put Option. _Advances in Futures and Options Research_, _1_, 119–139.

Margrabe W. (1978). The Value of an Option to Exchange One Asset for the Other. _Journal of Finance_, _33_, 177–186.

Martellini L. (2000). Efficient Option Replication in the Presence of Transaction Costs. _Review of Derivatives Research_, _4_, 107–131.

Martellini L., & Priaulet P. (2002). Competing Methods for Option Hedging in the Presence of Transaction Costs. _Journal of Derivatives_, _9_, 26–38.

McDonald R., & Schr¨oder M. (1998). A Parity Result for American Options. _Journal of Computational Finance_, _1_, 5–13.

Melino A., & Turnbull S. (1995). Misspecification and the Pricing and Hedging of Long Term Foreign Currency Options. _Journal of International Money and Finance_, _14_, 373–393.

Merton R. (1976). Option Pricing with Discontinuous Returns. _Journal of Financial Economics_, _3_, 125– 144.

Merton R. (1973). Theory of Rational Option Pricing. _Bell Journal of Economics and Management Science_, _4_, 141–183.

Mohamed B. (1994). Simulation of Transaction Costs and Optimal Rehedging. _Applied Mathematical Finance_, _1_, 49–62.

Moraux F. (2019). On Bankruptcy Procedures and the Valuation of Corporate Securities. _Finance_, _40_(3), 141–191.

Nandi S. (1998). How Important is the Correlation between Returns and Volatility in a Stochastic Volatility Model? Empirical Evidence from Pricing and Hedging in the S&P 500 Index Options Market. _Journal of Banking and Finance_, _22_, 589–610.

Nelson D. (1990). ARCH Models as Diffusion Approximations. _Journal of Econometrics_, _45_, 7–38.

Nelson D. (1991). Conditional Heteroskedasticity in Asset Returns: A New Approach. _Econometrica_, _59_, 347–370.

Omberg E. (1987). The Valuation of American Puts with Exponential Exercise Policies. _Advances in Futures and Options Research_, _2_, 117–142.

Palmer K. (2001). A Note on the Boyle-Vorst Discrete-Time Option Pricing Model with Transactions Costs. _Mathematical Finance_, _11_, 357–363.

Platen E., & Schweizer M. (1998). On Feedback Effects from Hedging Derivatives. _Mathematical Finance_, _8_, 67–84.

Reiner E., & Rubinstein M. (1991). Breaking Down the Barriers. _Risk_, _4_, 31–35.

Rendleman R., & Bartter B. (1979). Two-State Option Pricing. _Journal of Finance_, _34_, 1093–1110.

Ritchken P., Sankarasubramanian L., & Vijh A. (1993). The Valuation of Path Dependent Contracts on the Average. _Management Science_, _39_, 1202–1213.

Ritchken P., & Trevor R. (1999). Pricing Options Under Generalized GARCH and Stochastic Volatility Processes. _Journal of Finance_, _54_, 377–402.

Rubinstein M. (1985). Nonparametric Tests of Alternative Option Pricing Models Using All Reported Trades and Quotes on the 30 Most Active CBOE Option Classes from August 23, 1976 through August 31, 1978. _Journal of Finance_, _40_, 455–480.

Rubinstein M. (1994). Implied Binomial Trees. _Journal of Finance_, _49_, 771–818.

Rubinstein M. (1998). Edgeworth Binomial Trees. _Journal of Derivatives_, _5_, 20–27.

Schmalensee R., & Trippi R. (1978). Common Stock Volatility Expectations Implied by Option Premia. _Journal of Finance_, _33_, 129–147.

Schr¨oder M. (1989). Computing the Constant Elasticity of Variance Option Pricing Formula. _Journal of Finance_, _44_, 211–219.

Shimko D. (1991). _Finance in Continuous Time: A Primer_. Kolb Publishing Company.

Shu J., & Zhang J. (2004). Pricing S&P 500 Index Options Under Stochastic Volatility with the Indirect Inference Method. _Journal of Derivatives Accounting_, _1_, 1–16.

Simonato J.-G. (2011). Johnson Binomial Trees. _Quantitative Finance_, _11_, 1165–1176.

Smith C. (1976). Option Pricing: A Review. _Journal of Financial Economics_, _3_, 3–54.

Stentoft L. (2004). Convergence of the Least Squares Monte Carlo Approach to American Option Valuation. _Management Science_, _50_, 1193–1203.

Stoll H. (1969). The Relationship Between Put and Call Option Prices. _Journal of Finance_, _24_, 801–824.

Stulz R. (1982). Options on the Minimum or the Maximum of Two Risky Assets. _Journal of Financial Economics_, _10_, 161–185.

Tian Y. (1993). A Modified Lattice Approach to Option Pricing. _Journal of Futures Markets_, _13_, 563–577. Tian Y. (1999). A Flexible Binomial Option Pricing Model. _Journal of Futures Markets_, _19_, 817–843.

Toft K. (1996). On the Mean-Variance Trade-Off in Option Replication with Transaction Costs. _Journal of Financial and Quantitative Analysis_, _31_, 233–263.

Turnbull S., & Wakeman L. (1991). A Quick Algorithm for Pricing European Average Options. _Journal of Financial and Quantitative Analysis_, _26_, 377–389.

Widdicks M., Andricopoulos A., Newton D., & Duck P. (2002). On the Enhanced Convergence of Standard Lattice Methods for Option Pricing. _Journal of Futures Markets_, _22_, 315–338.

Wiggins J. (1987). Option Values under Stochastic Volatility: Theory and Empirical Estimates. _Journal of Financial Economics_, _19_, 351–372.

Wilmott P. (1994). Discrete Charms. _Risk_, _7_, 48–51.

Wilmott P. (2000). _Paul Wilmott on Quantitative Finance_. Wiley, Chichester.

46 _Derivatives, by Dorion and Fran¸cois, Sunday 24<sup>th</sup> August, 2025_

**Chapter 2**

# Diffusion model

In this chapter, we review the standard mathematical tools involved in the pricing of derivatives in continuous time. We first describe the dynamics of the UA price and introduce the fundamental stochastic process used for modeling these dynamics, namely the Brownian motion. Next, we present Itˆo’s lemma, which characterizes the rules of differential calculus in the presence of Brownian motions. The application of Itˆo’s lemma, combined with a no-arbitrage argument, leads to a valuation rule for derivatives resorting to Partial Differential Equations (PDE). Alternatively, solving the PDE is equivalent to computing an expectation under a modified probability measure. The equivalence between these two valuation methods is shown in the Feynman-Kac theorem.

## 2.1 Asset price dynamics

We consider an UA traded in continuous time on an arbitrage-free financial market. The market price of the UA is a stochastic process _<sub>{S</sub>_(_<sub>t</sub>_)_<sub>}t≥</sub>_<sub>0</sub> that we aim to characterize. We focus our attention on the time interval \[_<sub>t</sub> −_ <sub>∆</sub>_<sub>t,t</sub>_\] that we discretize into _<sub>N</sub>_ periods of equal length _<sub>h</sub>_. Let _{<sub>z</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> denote the stochastic process representing the UA return and <sub>∆</sub>_<sub>zn</sub>_ denote the change in UA return over the _<sub>n</sub>_<sup>th</sup> time period, that is

∆_z<sub>n</sub>_ \= _z_(_t−_∆_t_ \+ _nh_) _− z_(_t−_∆_t_ \+ (_n −_ 1)_h_) _∀n_ \= 1_,...,N._

The figure below displays the time discretization of the interval \[_<sub>t −</sub>_ <sub>∆</sub>_<sub>t,t</sub>_\].

47

0

_t_

_t_

_t_

_T_

_h_

\[

_N_

\=

_t_

/

_h_

\]

Figure 2.1: Example of a Brownian motion. To characterize the UA price dynamics, we rely on the fundamental assumption that the changes in return _{_<sub>∆</sub>_<sub>zn}</sub>_ are independent and identically distributed (i.i.d.).

The independence assumption means that the change in return between dates _<sub>t</sub>_ \+ (_<sub>n −</sub>_ 1)_<sub>h</sub>_ and _<sub>t</sub>_ \+ _<sub>nh</sub>_ has no influence on the change in return between dates _<sub>t</sub>_ \+ _<sub>nh</sub>_ and _<sub>t</sub>_ \+ (_<sub>n</sub>_ \+ 1)_<sub>h</sub>_. Such a return process is said to be Markovian (i.e., without memory). The identical distribution assumption entails that the source of randomness affecting returns remains the same over the time interval \[0_<sub>,T</sub>_\]. These two assumptions are consistent with the weak form of market efficiency.

We further assume that the distribution of _<sub>{</sub>_<sub>∆</sub>_<sub>zn}</sub>_ admits a mean and a variance given by

E \[∆_z<sub>n</sub>_\] = _λ,_

Var (∆_z<sub>n</sub>_) = _υ_<sup>2</sup>_._

Under that assumption, the _continuously compounded_ return on \[_<sub>t −</sub>_ <sub>∆</sub>_<sub>t,t</sub>_\] is

_N N_

_Z<sub>t−</sub>_<sub>∆</sub>_<sub>t,t</sub>_ \= <sup>X</sup> _z_(_t_ \+ _nh_) _− z_(_t_ \+ (_n −_ 1)_h_) = <sup>X</sup>∆_z<sub>n</sub>._

_n_\=1 _n_\=1

This _discrete time_ process has mean and variance

" _N_ #

E \[_Z<sub>t−</sub>_<sub>∆</sub>_<sub>t,t</sub>_\] = E <sup>X</sup>∆_z<sub>n</sub>_ \= _Nλ_ \= _µ_∆_t,_

_n_\=1

_N_ ! _N_

Var (_Z<sub>t−</sub>_<sub>∆</sub>_<sub>t,t</sub>_) = Var <sup>X</sup>∆_z<sub>n</sub>_ \= <sup>X</sup> Var (∆_z<sub>n</sub>_) = _Nυ_<sup>2</sup> \= _σ_<sup>2</sup>∆_t,_

_n_\=1 _n_\=1

where _µ_ \= _λ/h_ and _σ_<sup>2</sup> \= _υ_<sup>2</sup>_/h_. Thus,

1\. Returns _<sub>Zt−</sub>_<sub>∆</sub>_<sub>t,t</sub>_ have a mean and a variance that are constant per unit of time and equal to _<sub>µ</sub>_ and _σ_<sup>2</sup>, respectively. For all (_<sub>s,t</sub>_) with _<sub>s > t</sub>_, the mean and the variance of _<sub>Zt,s</sub>_ are proportional to _<sub>s</sub>−<sub>t</sub>_.

In particular, for all _<sub>T</sub>_

E(_Z_<sub>0</sub>_<sub>,T</sub>_ ) = _µT,_

V_ar_(_Z_<sub>0</sub>_<sub>,T</sub>_ ) = _σ_<sup>2</sup>_T._ 2\. As _<sub>N</sub> → ∞_, the return _<sub>Z</sub>_<sub>0</sub>_<sub>,T ,T</sub> ≥_ 0_<sub>,</sub>_ exhibits a Gaussian distribution since, from central limit theorem, the increments

_N_

_Zt−_∆_t,t_ \= lim X∆_zn_

_N→∞_

_n_\=1 are normally distributed.

We now turn to modelling the UA price dynamics. The (ex-dividend) return _<sub>Zt−</sub>_<sub>∆</sub>_<sub>t,t</sub>_ can be written as

\= _S_(_t_)_S−_(_tS−_(_t_∆_−t_)∆_t_)_,_

_Zt−_∆_t,t_

and we know it is normally distributed with mean _<sub>µ</sub>_<sub>∆</sub>_<sub>t</sub>_ and variance _<sub>σ</sub>_<sup>2</sup><sub>∆</sub>_<sub>t</sub>_. Denote _<sub>ε</sub>_ a random variable with standard normal distribution. We can write the following

_√ S_(_t_) _− S_(_t −_ ∆_t_) = _S_(_t −_ ∆_t_)_µ_∆_t_ \+ _S_(_t −_ ∆_t_)_σ_ ∆_tε,_

or

∆_S_(_t_) = _S_(_t −_ ∆_t_)_µ_∆_t_ \+ _S_(_t −_ ∆_t_)_σ_∆_W_(_t_)_,_

where _{<sub>W</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> is a stochastic process yet to be determined. Since the increments <sub>∆</sub>_<sub>S</sub>_(_<sub>t</sub>_)_<sub>/S</sub>_ are independent and Gaussian with mean _<sub>µ</sub>_<sub>∆</sub>_<sub>t</sub>_ and variance _<sub>σ</sub>_<sup>2</sup><sub>∆</sub>_<sub>t</sub>_, we obtain that _{<sub>W</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> is a stochastic process with independent increments, normally distributed with zero mean and a variance proportional with the passage of time.

Taking the continuous time limit <sub>∆</sub>_<sub>t →</sub>_ 0<sup>+</sup>, the former equation takes the form of a _Stochastic Differential Equation_ (SDE)

d_S_(_t_) = _µS_(_t_)d_t_ \+ _σS_(_t_)d_W_(_t_)_,_

and the UA price process is called a _Geometric Brownian Motion_ (GBM).<sup><sup>[\[1\]](#footnote-1)</sup></sup>

More generally, when the trend (_<sub>µ</sub>_) and volatility (_<sub>σ</sub>_) parameters are not constant, the stochastic process driven by a Brownian motion is referred to as a _diffusion process_.

**Definition 2.1** _The dynamics of the UA price in continuous time is called a diffusion or an Itˆo process when it can be written as_ d_S_(_t_) = _µ_(_S,t_) d_t_ \+ _σ_ (_S,t_) d_W_(_t_)_,_ (2.1)

_where {<sub>W</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> _is a standard Brownian motion._

To ensure the existence of a unique strong solution to the diffusion, the drift function _<sub>µ</sub>_(_<sub>S,t</sub>_) as well as the volatility function _<sub>σ</sub>_ (_<sub>S,t</sub>_) must satisfy the Lipschitz continuity condition, i.e., there exists a constant _k_ such that for all real numbers (_<sub>x,y</sub>_)

_|µ_(_x,t_) _− µ_(_y,t_)_|_ \+ _|σ_(_x,t_) _− σ_(_y,t_)_| ≤ k |x − y|._

## 2.2 The Brownian motion

This process derives its name from botanist Robert Brown who studies in 1828 the irregular movements of pollen particles over the water surface. In 1900, Louis Bachelier proves the Markovian feature of the Brownian motion and uses this process to model stock prices (and not returns). In physics, some properties of the Brownian motion are examined by Albert Einstein in 1905, and deeper study is undertaken by Nicolas Wiener in 1923 and by Paul L´evy in 1948. We will limit our presentation to some fundamental results.

**Definition 2.2** _A Brownian motion {<sub>W</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> _is a real-valued stochastic process such that_

1.  _<sub>W</sub>_(0) = 0_<sub>,</sub>_
2.  _∀<sub>s,t</sub> with <sub>t > s</sub>, <sub>W</sub>_(_<sub>t</sub>_) _− <sub>W</sub>_(_<sub>s</sub>_) _is a Gaussian random variable with zero mean and variance <sub>t</sub> − <sub>s</sub>,_
3.  _∀t_<sub>0</sub> _< t_<sub>1</sub> _< ... < t<sub>N</sub>, variables_ (_W_(_t<sub>n</sub>_) _− W_(_t<sub>n−</sub>_<sub>1</sub>)) _are independent from one another._

**Theorem 2.3** _Paths of the Brownian motion are continuous, nowhere differentiable, and do not display bounded variations._

The proof of this theorem is beyond the scope of this book. Rather, we put forward the following heuristic arguments. Continuity is a direct consequence of the Brownian motion being defined as a continuous time process without any jumps. Paths are not differentiable because the Brownian motion is constantly changing its course. The Brownian motion trajectory can be viewed as a series of peaks. It is therefore necessary to define a new integration rule with respect to the Brownian motion as the standard Lebesgue integral is not defined in this case. Finally, since the increments of the Brownian motion follow a normal distribution, they are unbounded by definition.

**Definition 2.4** _A stochastic process is called a martingale with respect to a given information set if its time-<sub>t</sub> expectation, conditional on the information available at time <sub>s < t</sub>, is equal to the value of this process at time <sub>s</sub>. That is, the process {<sub>M</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> _is a martingale if_

_∀s,t with s < t,_ E_<sub>s</sub>_ \[_M_(_t_)\] = _M_(_s_)_._

The notion of martingale refers to a process whose present value is the best predictor of its future value. This notion is essential to financial theory. As put forward by Fama (1970), the unanticipated return variations of assets traded on an efficient financial market should be martingales.

Similarly, a process is said to be a submartingale if

_∀s,t_ with _s < t,_ E_<sub>s</sub>_ \[_M_(_t_)\] _≥ M_(_s_)_._

and a supermartingale if

_∀s,t_ with _s < t,_ E_<sub>s</sub>_ \[_M_(_t_)\] _≤ M_(_s_)_._

**Proposition 2.5** _Let {W_(_t_)_}<sub>t≥</sub>_<sub>0</sub> _denote a standard Brownian motion. {W_(_t_)_}<sub>t≥</sub>_<sub>0</sub> _is a martingale with respect to the information contained in its trajectory (also referred to as the natural filtration). The same holds for the process_ exp<sup>n</sup>_<sub>λW</sub>__<sub>t</sub>_<sup>o</sup> _where <sub>λ</sub> is an arbitrary constant._

**Proof** _∀s,t_ with _s < t_

E_<sub>s</sub>_ \[_W_(_t_) _− W_(_s_)\] = E \[_W_(_t_) _− W_(_s_)\] = 0_._

First equality stems from the independent increments of the Brownian motion. Second equality results from the centered distribution of the Brownian motion. Besides,

E_<sub>s</sub>_ \[_W_(_t_) _− W_(_s_)\] = E_<sub>s</sub>_ \[_W_(_t_)\] _−_ E_<sub>s</sub>_ \[_W_(_s_)\] = E_<sub>s</sub>_ \[_W_(_t_)\] _− W_(_s_)_._

The last equality holds because the realization of the Brownian motion at time _<sub>s</sub>_ is measurable with respect to the information available at that same time (the process is said to be adapted). Combining the two preceding equalities yields

E_<sub>s</sub>_ \[_W_(_t_)\] = _W_(_s_)_._

As far as exp<sup>n</sup>_<sub>λW</sub>_(_<sub>t</sub>_) _− <sup>λ</sup>_<sub>2</sub><sup>2</sup> _<sub>t</sub>_<sup>o</sup> is concerned, the characteristic function theorem entails that _∀<sub>s,t</sub>_ with _<sub>s < t</sub>_, given that _<sub>W</sub>_(_<sub>t</sub>_) is Gaussian,

E_s_ "exp(_λW_(_t_) _− λ_22 _t_)# = exp(E_s_ "_λW_(_t_) _− λ_22 _t_\# +  Vars _λW_(_t_) _− λ_22 _t_!)

\= exp(_λW_(_s_) _− λ_22 _t_ \+ _λ_22 (_t − s_))

\= exp(_λW_(_s_) _− λ_22 _s_)_._ □

We now turn to the theory of stochastic integration. Let Λ denote the set of “step” functions from R<sup>\+</sup> to R, i.e., all functions _<sub>fN</sub>_ that can be written as

_N fN_ (_t_) = X _an_1_t ∈_ \]_tn−_1_,tn_\]_._

_n_\=1

for 0 = _<sub>t</sub>_<sub>0</sub> _<sub>< t</sub>_<sub>1</sub> _<sub>< ... < tN</sub>_ \= _<sub>T</sub>_. These functions can be represented as follows

_t_

1

_t_

2

_t_

3

_t_

4

_a_

1

_a_

2

_a_

3

_a_

4

\]

\]

\]

\]

\]

\]

\]

Figure 2.2: Example of a step function.

For that class of functions, we define the integral _<sub>IfN</sub>_ as

<sub>Z</sub> _T N_

_I<sub>fN</sub>_ (_T_) = _f<sub>N</sub>_ (_t_) d_W_(_t_) = <sup>X</sup> _a<sub>n</sub>_ (_W<sub>tn</sub> − W_(_t<sub>n−</sub>_<sub>1</sub>))_._

<sup>0</sup> _n_\=1

Let us now consider Λ, the set of square integrable functions _<sub>f</sub>_ from R<sup>\+</sup> to R, that is, such that

<sup>R</sup>) d_<sub>t <</sub>_ +_<sub>∞</sub>_. It can be shown that there exists a series of functions _<sub>fN ∈</sub>_ Λ that converge towards _f_ in the sense that

Z _T_

(_f<sub>N</sub>_ (_t_) _− f_ (_t_))<sup>2</sup> d_t →_ 0_._

0

Assuming the series of integrals _<sub>IfN</sub>_ (_<sub>T</sub>_) converge towards a finite limit denoted by _<sub>If</sub>_(_<sub>T</sub>_), then the stochastic integral of _<sub>f</sub>_ can simply be defined as

Z _T_

_I<sub>f</sub>_ (_T_) = _f_ (_t_) d_W_(_t_)_._

0

Such a stochastic integral is called a _Wiener integral_.

**Proposition 2.6** _For all square integrable functions <sub>f</sub> and <sub>g</sub>, the Wiener integrals have the following properties:_

1.  _<sub>If</sub>_ (_<sub>t</sub>_) _is a centered Gaussian random variable._
2.  _For α and β two scalars, I<sub>αf</sub>_<sub>+</sub>_<sub>βg</sub>_(_t_) = _αI<sub>f</sub>_ (_t_) + _βI<sub>g</sub>_ (_t_)_._
3.  E h_If_2 (_t_)i = R0_t f_2 (_u_) d_u._
4.  E \[_I<sub>f×g</sub>_(_t_)\] = <sup>R</sup><sub>0</sub>_<sup>t</sup> f_ (_u_)_g_ (_u_) d_u._

The results from the proposition above can be extended to the case where _<sub>f</sub>_ and _<sub>g</sub>_ belong to a certain class of stochastic processes. More precisely, let _<sub>{θ</sub>_(_<sub>t</sub>_)_<sub>}t≥</sub>_<sub>0</sub> denote a left-continuous, adapted stochastic process with E <sup>hR</sup> d_<sub>s</sub>_<sup>i</sup> _<sub><</sub>_ +_<sub>∞</sub>_, then the stochastic integral

Z _t_

_I<sub>θ</sub>_ (_t_) = _θ_(_s_)d_W_(_s_)

0

is well defined. It is referred to as an _Itˆo integral_.

**Proposition 2.7** _For all left-continuous, adapted, square integrable processes {<sub>θ</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub>_, the Itˆo integral verifies the following properties:_

1.  _<sub>Iθ</sub>_(_<sub>t</sub>_) _is a continuous, adapted process._
2.  _<sub>Iθ</sub>_(_<sub>t</sub>_) _is a martingale._
3.  _I<sub>θ</sub>_<sup><sup>[\[2\]](#footnote-2)</sup></sup>(_t_) _−_ <sup>R</sup><sub>0</sub>_<sup>t</sup> θ_<sup>2</sup>(_s_)d_s is a martingale._

In particular, we obtain

Z _t_

E h_Iθ_2(_t_)i = E _θ_2(_s_)d_s ,_

0

and, given _{<sub>θ</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> and _{<sub>ϕ</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> two left-continuous, adapted, square integrable process, we get

<sup>Z</sup> _t_

E \[_I<sub>θ</sub>_(_t_) _× I<sub>ϕ</sub>_(_t_)\] = E _θ_(_s_)_ϕ_(_s_)d_s ._

0

## 2.3 Itoˆ’s lemma

### 2.3.1 One-dimensional case

Consider an UA price driven by a diffusion process<sup>2</sup>

d_S_ \= _µ_(_S,t_)_dt_ \+ _σ_ (_S,t_) d_W._

A fundamental result, called Itˆo’s lemma and proved in Itˆo (1944), relates the change in the value of a contingent claim (derivative instrument) to changes in the value of the UA.<sup><sup>[\[3\]](#footnote-3)</sup></sup> Specifically,

**Lemma 2.8** _(Itˆo) Let the process {<sub>x</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> _be driven by the following diffusion_

d_x_ \= _µ_(_x,t_)_dt_ \+ _σ_ (_x,t_) d_W._

_For all functions <sub>g</sub>_ (_<sub>x,t</sub>_) _twice differentiable with respect to <sub>x</sub> and once differentiable with respect to <sub>t</sub>,_

d_g_ ) d_W._

**Proof** Below is a sketch of proof. The second order Taylor expansion of _<sub>g</sub>_ (_<sub>x,t</sub>_) yields

_∂g_

<sup>∆</sup>_<sup>g</sup> ≃_ ∆_t_ \+ _∂g_<sup>∆</sup>_<sup>x</sup>_ \+ 12 _∂∂t_2_g_<sup>2</sup> (<sup>∆</sup>_<sup>t</sup>_)<sup>2</sup> \+ <sub>2</sub>1 _∂x∂_2_g_<sup>2</sup> (<sup>∆</sup>_<sup>x</sup>_)<sup>2</sup> \+ _∂x∂t∂_2_g_ <sup>∆</sup>_<sup>x</sup>_<sup>∆</sup>_<sup>t.</sup>_

_∂t ∂x_

Terms in (<sub>∆</sub>_<sub>t</sub>_)<sup>2</sup> and in <sub>∆</sub>_<sub>x</sub>_<sub>∆</sub>_<sub>t</sub>_ are of order strictly greater than 1. Hence they get negligible at the continuous time limit. However, in contrast to standard differential calculus, terms in (<sub>∆</sub>_<sub>x</sub>_)<sup>2</sup> are not. Indeed,

∆_x_ \= _µ_∆_t_ \+ _σ_ \[_W_(_t_) _− W_(_t −_ ∆_t_)\]

_√_ \= _µ_∆_t_ \+ _σε_ ∆_t._

Consequently,

(∆_x_)<sup>2</sup> _≃ σ_<sup>2</sup>_ε_<sup>2</sup>∆_t._

The expectation yields

E <sup>h</sup>(∆_x_)<sup>2i</sup> \= _σ_<sup>2</sup>∆_t_E <sup>h</sup>_ε_<sup>2i</sup> \= _σ_<sup>2</sup>∆_t,_

since _<sub>ε</sub>_ has zero mean and unit variance. Moreover,

Var (∆_x_)2 = _σ_4(∆_t_)2 Var _ε_2_,_

which is a term of order 2 becoming negligible as <sub>∆</sub>_<sub>t →</sub>_ 0\. Hence the term in (<sub>∆</sub>_<sub>x</sub>_)<sup>2</sup> gets non-stochastic in the continuous time limit (its variance gets to zero) and is worth its expectation _<sub>σ</sub>_<sup>2</sup>_<sub>dt</sub>_. Plugging this value into the Taylor expansion and taking the continuous time limit, we obtain

d_g_  d_t,_

which yields Itˆo’s lemma.□

**Example 2.9 (Geometric Brownian motion)** _Assuming that the dynamics of the UA price is given_

_by_

_dS_

\= _µdt_ \+ _σdW, S the solution to this SDE is obtained by applying Itˆo’s lemma to the function <sub>F</sub>_(_<sub>x,t</sub>_) = ln_<sub>x</sub>:_

d(ln_S_) = 1 _µS −_ 12 _<sub>S</sub>_1<sub>2</sub> _σ_<sup>2</sup>_S_<sup>2</sup> d_t_ \+ _<sub>S</sub>_1 _σS_ d_W, <sub>S</sub>_

_σ_2 ! d(ln_S_) = _µ −_ 2 d_t_ \+ _σ_ d_W._

_Integrating on both sides_

_σ_2 ! ln_S_(_t_) = ln_S_(0) + _µ −_ 2 _t_ \+ _σW_(_t_)_,_

_hence_

_S_(_t_) = _S_(0)exp<sup>(</sup> _<sub>µ −</sub> <sup>σ</sup>_2<sup>2 !</sup>_<sub>t</sub>_ \+ _σW_(_t_)<sup>)</sup>_<sub>.</sub>_ (2.2)

_The latter equation confirms that the UA price is log-normally distributed when the continuously compounded returns are assumed to be normal._

### 2.3.2 Itoˆ’s product

Alternatively, Itˆo’s lemma can be expressed in a compact form

d_g_ _,_

and the latter equation can be expanded using the rules of Itˆo’s product. These rules can be summarized in the following table, where _<sub>W</sub>_(_<sub>t</sub>_) and _<sub>Z</sub>_(_<sub>t</sub>_) denote two Brownian motions with correlation coefficient _<sub>ρ</sub>_:

|     |     |     |
| --- | --- | --- |
|     | d_<sub>t</sub>_ d | _W_(_t_) |
| d_t_ | 0   | 0   |
| d_Z_(_t_) | 0   | _ρ_d_t_ |

A heuristic proof goes as follows. Consider the product <sub>∆</sub>_<sub>t ·</sub>_ <sub>∆</sub>_<sub>W</sub>_(_<sub>t</sub>_). From the definition of the Brownian motion, we have the following equality in law

_√_ ∆_t ·_ ∆_W_(_t_) = ∆_t ·_ ∆_tε_ \= (∆_t_)<sup>3</sup>_<sup>/</sup>_<sup>2</sup> _ε._

This term becomes zero in the continuous time limit. Similarly, we have the following equality in law

_√ √_ ∆_Z_(_t_) _·_ ∆_W_(_t_) = ∆_tε_<sub>1</sub> ∆_tε_<sub>2</sub> \= ∆_tε_<sub>1</sub>_ε_<sub>2</sub>_._

The mean and variance of that random variable are

E \[∆_tε_<sub>1</sub>_ε_<sub>2</sub>\] = _ρ_∆_t,_

Var (∆_tε_<sub>1</sub>_ε_<sub>2</sub>) = (∆_t_)<sup>2</sup> Var (_ε_<sub>1</sub>_ε_<sub>2</sub>)_._

In the continuous time limit, the variance becomes zero and the variable therefore converges to _<sub>ρ</sub>_d_<sub>t</sub>_. Using Itˆo’s product, we can recover Itˆo’s lemma from expanding its compact version. Indeed,

d_g_ 

_._

### 2.3.3 Multi-dimensional case

Consider a more general economy with _<sub>NA</sub>_ traded underlying assets whose price process **_<sub>S</sub>_** \= _{<sub>Sj</sub>}<sub>j</sub>_<sub>\=1</sub>_<sub>,...,NA</sub>_ is subject to _<sub>NA</sub>_ sources of risk. The price process follows a _<sub>NA−</sub>_dimensional diffusion, that is, for each

_j_ \= 1_,...,N<sub>A</sub>_

d_S<sub>j</sub>_(_t_) = _µ<sub>j</sub>_ (**_S_**_,t_) d_t_ \+ _σ<sub>j</sub>_ (**_S_**_,t_) d_W<sub>j</sub>_(_t_)_,_

where _{<sub>Wj</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> are standard Brownian motions with correlation matrix d_<sub>Wj</sub> ·_ d_<sub>Wk</sub>_ \= _<sub>ρjk</sub>_ d_<sub>t</sub>_ for all _<sub>j</sub>_ \=_̸ <sub>k</sub>_. For convenient notations, we drop the drift and volatility coefficients’ dependence on **_<sub>S</sub>_** and _<sub>t</sub>_.

Consider a derivative instrument written on the _<sub>NA</sub>_ assets **_<sub>S</sub>_** whose value function is denoted by _<sub>g</sub>_.

From Itˆo’s lemma, the dynamics of _<sub>g</sub>_ is given by

d_g_ \= _∂g∂t_ \+ X _∂S∂g µj_ \+ 12 X_j_ X_k ∂S∂j_2_∂Sg k σjσkρjk_ d_t_ _j j j_ d_Wj._

_j j_

## 2.4 Partial differential equation

Back to the one-dimensional case, we consider a derivative instrument with value _<sub>g</sub>_ (_<sub>S,t</sub>_) depending on UA price and time. Suppose the UA price process _<sub>S</sub>_ follows a diffusion as in equation (2.1). We construct the arbitrage portfolio _<sub>P</sub>_ consisting in selling one unit of the derivative and buying _<sub>h</sub>_ units of the UA. We require that portfolio _<sub>P</sub>_ be _self-financing_. Under that constraint, the change in value of the portfolio is

d_P_ \= _−_d_g_ \+ _h_d_S._

According to Itˆo’s lemma,

d_P_ 

Setting _<sub>h</sub>_ \= _<sub>∂S</sub><sup>∂g</sup>_ , stochastic terms in _<sub>dW</sub>_(_<sub>t</sub>_) cancel out:

! d_P_d_t._

Note that the terms in _<sub>µ</sub>_(_<sub>S,t</sub>_)d_<sub>t</sub>_ disappear as well. Portfolio _<sub>P</sub>_ is therefore locally riskless and, in AoA, must earn the risk-free rate, i.e.,

d_P_ \= _rP_ d_t,_

which yields

_rP_ _,_

or, rearranging terms,

 _rg._ (2.3)

Equation (2.3) is a Partial Differential Equation (PDE). It is obtained by application of Itˆo’s lemma and the AoA principle. Solving the PDE allows to determine the value of _<sub>g</sub>_. Boundary conditions are further required to fully characterize the pricing problem and thus obtain a unique solution. In finance, such boundary conditions are typically terminal conditions reflecting the terminal payoff associated with the type of derivative instrument under study.

Depending on the complexity of the derivative and on the sophistication of the UA price dynamics, some PDEs associated with their boundary conditions have an explicit solution (this is the case for the European option written on an UA whose price is driven by a GBM), while others have not.

It is noteworthy that the PDE resulting from the diffusion model indicates that the value of the derivative depends on

1.  time (_<sub>t</sub>_),
2.  the constant risk-free rate (_<sub>r</sub>_),
3.  the current UA price (_<sub>S</sub>_),
4.  the volatility function of the UA (_<sub>σ</sub>_ (_<sub>S,t</sub>_)).

All these variables are independent from agents’ risk preferences. In particular, we note that the term _<sub>µ</sub>_(_<sub>S,t</sub>_), which incorporates a risk premium determined by agents’ risk aversion, does not appear in the PDE. This observation is important as it motivates the notion of risk-neutral pricing which we now elaborate on.

## 2.5 Risk-neutral approach

### 2.5.1 Intuition

The pricing PDE, obtained from the AoA principle, indicates that the valuation of a derivative does not involve the agents’ risk preferences. In this line of reasoning, Cox and Ross (1976) argue that, without any loss in generality, the valuation problem can be tackled from the viewpoint of a risk-neutral individual. Two major adjustments must then be made.

1.  From the risk-neutral individual’s perspective, the UA must earn the risk-free rate _<sub>r</sub>_ instead of _<sub>µ</sub>_ (since no risk premium is demanded). Thus,

_S_(_t_) = E<sub>e</sub><sup>h</sup>_S_(0)_e<sup>rt</sup>_<sup>i</sup>_,_

where E \[<sub>e</sub> _<sub>.</sub>_\] stands for the expectation operator associated with the probability measure used by the risk-neutral individual.

1.  The discount rate for all future cash flows must be the risk-free rate _<sub>r</sub>_ (since, again, no risk premium is demanded).

Hence the value of a European-style derivative can be computed as the expectation of its terminal payoff, discounted at the risk-free rate. But the expectation must be taken under the probability measure used by the risk-neutral individual

_g_(_t_) = Ee<sup>h</sup>_g_ (_T_)_e−r_(_T−t_)<sup>i</sup>_._

Put differently, the process _<sub>g</sub>_(_<sub>t</sub>_)_<sub>e</sub><sup>−rt</sup>_ is a martingale under that specific probability measure, which has often been referred to as the “risk-neutral probability” or, more accurately, the _Equivalent Martingale Measure_ (EMM).

The derivatives risk-neutral valuation principle has been discussed in Smith (1976) and Cox and Ross (1976), then formally studied in Harrison and Kreps (1979) and Harrison and Pliska (1981). The next subsection presents the mathematical tool that allows to characterize the EMM.

### 2.5.2 Girsanov theorem

Under the historical (physical) probability measure (i.e., the probability measure under which the risk averse, representative agent is reasoning), denoted by P, agents include a risk premium for holding the UA and therefore demand the instantaneous expected return _<sub>µ</sub>_. Assume that the UA price is

 (Z _t_ ! Z _t_ )

_S_(_t_) = _S_(0)exp _µ −_d_u_ \+ _σ_ (_S,u_) d_W<sub>u</sub> ._

00

In a world with risk-neutral individuals, agents do not require any risk premium and the instantaneous expected return on the UA must be _<sub>r</sub>_ in the AoA. Hence pricing from the risk-neutral individual’s perspective involves a correction in the UA price drift (from _<sub>µ</sub>_ to _<sub>r</sub>_). Girsanov theorem explicitly shows that this is equivalent to reasoning under a different probability measure.

**Theorem 2.10 (Girsanov)** _Under probability measure_ P_, consider {W_(_t_)_}<sub>t≥</sub>_<sub>0</sub> _a standard Brownian motion and {<sub>η</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> _a square integrable, adapted stochastic process (such that_ E d_<sub>s</sub>_<sup>oi</sup> _<sub><</sub>_

+_∞). Define_

 ( <sup>Z</sup> _T_<sup>Z</sup> _T_ )

_ξ_(_T_) = exp _− η_(_s_)d_W_(_s_) _−η_<sup>2</sup>(_s_)d_s ,_

00

_and denote_ Q _the probability measure, equivalent to_ P_, defined by_

ddQP = _ξ_(_T_)_._

_Then, under_ Q_, the process_ <sup>n</sup>_<sub>W</sub>_Q(_<sub>t</sub>_)<sup>o</sup>_t≥_0 _defined by_

Z _t_

_W_)d_s_

_is a Brownian motion._

Remark: Two probability measures are said to be equivalent when their sets of zero probability events are the same.

Let us apply the Girsanov theorem to the UA price process _<sub>S</sub>_ with

_ξ_(_T_) = exp(_−_Z _T σµ_(_−S,tr_) d_W_(_t_) _−_Z0_T σµ_(_−S,tr_)2 d_t_)_,_

0

that is, the process _{<sub>η</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> is the market price of risk (Sharpe ratio)

_µ − r η_(_t_) _≡ σ_ (_<sub>S,t</sub>_)_._

Then, the UA price can be written as

(Z _t_ ! )

_S_(_t_) = _S_(0)exp _µ_d_u_

0

<sup>Z</sup> _t_  _<sup>− r</sup>_

_×_exp _σ_ (_S,u_) d_W_ (_u_) _− σ_ (_S,u_) _σ_ (_<sub>S,u</sub>_) d_u ,_

0 0

where <sup>n</sup>_<sub>W</sub>_<sup>Q</sup>(_<sub>t</sub>_)<sup>o</sup> _≥_0 is a Brownian motion under Q. Which yields

_t_

(<sup>Z</sup> _t_

_S_(_t_) = _S_(0)exp _<sub>r,</sub>_

0

i.e., under the EMM Q, the UA price is driven by a GBM with drift _<sub>r</sub>_ and same volatility function.

## 2.6 Feynman-Kac theorem

In the AoA, derivatives can be valued either by solving a PDE with appropriate boundary conditions, or by applying the martingale property under the EMM. By the law of one price, these two approaches must be equivalent. The Feynman-Kac theorem establishes that equivalence.

Consider the derivative with value _<sub>g</sub>_ (_<sub>S,t</sub>_) that is solution to

_,_ (2.4)

|     |     |     |
| --- | --- | --- |
| with terminal condition |     |     |
|     | _g_ (_S,T_) = _f_ (_S_)_._ | (2.5) |

Then the following theorem holds.

**Theorem 2.11 (Feynman-Kac)** _The unique solution to PDE (2.4) associated with boundary condition_

_(2.5)_

_g_ \= E h_e−rT f ZS_(_T_)i_,_

_where <sub>Zt</sub><sup>S</sup>_ (_<sub>S</sub>_) _is the stochastic process starting from <sub>S Z</sub><sup>S</sup>_(0) = _<sub>S</sub>_ _and driven by the following SDE_

d_Z<sup>S</sup>S_((_t_)_t_) = _r_d_t_ \+ _σ_ d_W_(_t_)_._

_Z_

**Proof** This is only a sketch of proof. For any date _<sub>u</sub>_ between 0 and _<sub>T</sub>_, we apply Itˆo’s lemma to the process _<sub>e</sub><sup>r</sup>_<sup>(</sup>_<sup>T−u</sup>_<sup>)</sup>_<sub>g Z</sub><sup>S</sup>_(_<sub>u</sub>_)_<sub>,u</sub>_, then we integrate between 0 and _<sub>T</sub>_. We obtain

_g Z<sup>S</sup>_(_T_)_,T_ _− e<sup>rT</sup> g Z<sup>S</sup>_(0)_,_0

_∂g Z_

\= Z _T er_(_T−u_)  _S_(_u_)_,u_ _S_ (_u_)_,u_ d_u_

_− rg Z_

0 _∂u_

<sup>Z</sup> _T_  _S_(_u_)_,u_

_∂g Z_

\+ _er_(_T−u_) <sub> </sub>_rS_ d_u_

0 _∂S_

_∂_

<sup>Z</sup> _<sup>T</sup>_ 1  2_g ZS_(_u_)_,u_ 2 2 d_u_

\+ _er_(_T−u_) 2 <sub></sub> _<sub>∂S</sub>_<sub>2 </sub>_σ S_

<sub>0</sub>

Z _T_ _∂g ZS_(_u_)_,u_

\+ _er_(_T−u_)  _σS_ d_W_(_u_)_._

0 _∂S_

Since _<sub>g</sub>_ is solution to PDE (2.4), the first three integrals cancel out. The fourth one is a Wiener integral (hence with zero mean). Taking expectations on both sides of the equation

E h_g ZS_(_T_)_,T_ _− erT g ZS_(0)_,_0i = 0_,_

or, alternatively,

E h_e−rT g ZS_(_T_)_,T_i = _g ZS_(0)_,_0_._

Thus

E h_e−rT f ZS_(_T_)i = _g_ (_S,_0) = _g,_

which ends the proof. □

The Feynman-Kac theorem states that to solve PDE (2.4), one must:

1.  define the process _<sub>Z</sub><sup>S</sup>_(_<sub>t</sub>_), which is equivalent to reasoning under a risk-neutral world,
2.  apply the terminal condition on that process,
3.  discount the terminal payoff with the risk-free rate,
4.  and take the expectation under the historical probability measure.

This methodology is therefore equivalent to proceeding to a change in probability measure (using the Girsanov theorem), and applying the martingale property to the derivative value process discounted at the risk-free rate under that new measure.

## 2.7 Problem set

##### Exercise 2.1

Let _{<sub>B</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> denote a standard Brownian motion. Show that _<sub>B</sub>_(_<sub>t</sub>_)<sup>2</sup> _− <sub>t</sub>_ is a martingale. More generally, prove that a convex function of a martingale is a submartingale.

##### Exercise 2.2

The stochastic process _<sub>{x</sub>_(_<sub>t</sub>_)_<sub>}t≥</sub>_<sub>0</sub> is characterized by the following SDE (known as the Arithmetic Brownian Motion or ABM): d_x_(_t_) = _µ_d_t_ \+ _σ_ d_W_(_t_)_._

Apply Itˆo’s lemma to the processes _<sub>U</sub>_ (_<sub>x,t</sub>_) = exp(_<sub>x</sub>_) and _<sub>V</sub>_ (_<sub>x,t</sub>_) = _<sub>t</sub>_exp(_<sub>x</sub>_).

##### Exercise 2.3

Consider _{<sub>x</sub>_<sub>1</sub>(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> and _{<sub>x</sub>_<sub>2</sub>(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> two real-valued, stochastic processes verifying

d_x_<sub>1</sub>(_t_) = _µ_<sub>1</sub> d_t_ \+ _σ_<sub>1</sub> d_W_<sub>1</sub>(_t_)_,_ d_x_<sub>2</sub>(_t_) = _µ_<sub>2</sub> d_t_ \+ _σ_<sub>2</sub> d_W_<sub>2</sub>(_t_)_,_

where _{<sub>Wj</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> (_<sub>j</sub>_ \= 1_<sub>,</sub>_2) are two Brownian motion with correlation coefficient _<sub>ρ</sub>_. Write down the SDE driving the process _<sub>F</sub>_ defined as

_F_ (_t,x_<sub>1</sub>_,x_<sub>2</sub>) = _x_<sub>1</sub> exp(_−x_<sub>2</sub>_t_)_._

##### Exercise 2.4

Adapted from Shimko (1991). The processes _{<sub>X</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> and _{<sub>Y</sub>_ (_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> are two GBM:

|     |     |     |
| --- | --- | --- |
| d_X_(_t_)<br><br>_X<sub>t</sub>_ | \=  | _α_d_t_ \+ _σ_ d_W_(_t_)_,_ |
| d_Y_ (_t_) | \=  | _β_ d_t_ \+ _v_ d_Z_(_t_)_,_ |

_Y<sub>t</sub>_

and d_W_(_t_)d_Z_(_t_) = _ρ_d_t._

1.  Show that _<sub>S</sub>_(_<sub>t</sub>_) = _<sub>X</sub>_(_<sub>t</sub>_)_<sub>Y</sub>_ (_<sub>t</sub>_) is a GBM.
2.  Show that _<sub>Ut</sub>_ \= _<sub>X</sub>_(_<sub>t</sub>_)_<sub>/Y</sub>_ (_<sub>t</sub>_) is a GBM.
3.  Consider the ordinary least-square regression of d_<sub>Y</sub>_ (_<sub>t</sub>_)_<sub>/Y</sub>_ (_<sub>t</sub>_) on d_<sub>X</sub>_(_<sub>t</sub>_)_<sub>/X</sub>_(_<sub>t</sub>_). What are the theoretical values for the slope, the constant and the _<sub>R</sub>_<sup>2</sup> coefficient?

## 2.8 Solutions

##### Solution 2.1

For two dates _<sub>s</sub>_ and _<sub>t</sub>_ with _<sub>s < t</sub>_, we compute

E_<sub>s</sub>_ <sup>h</sup>_B_(_t_)<sup>2</sup> _− t_<sup>i</sup> \= E_<sub>s</sub>_ <sup>h</sup>_B_(_t_)<sup>2i</sup> _− t._ Note that

Var<sub>s</sub> (_B_(_t_)) = E_<sub>s</sub>_ <sup>h</sup>_B_(_t_)<sup>2i</sup> _−_ E_<sub>s</sub>_ \[_B_(_t_)\]<sup>2</sup> _._

Hence

E_<sub>s</sub>_ <sup>h</sup>_B_(_t_)<sup>2</sup> _− t_<sup>i</sup> \= Var<sub>s</sub> (_B_(_t_)) + E_<sub>s</sub>_ \[_B_(_t_)\]<sup>2</sup> _− t_

\= (_t − s_) + _B_(_s_)<sup>2</sup> _− t_ \= _B_(_s_)<sup>2</sup> _− s,_

and the martingale property is verified.

Consider E_<sub>s</sub>_ \[_<sub>f</sub>_ (_<sub>Mt</sub>_)\] where _<sub>Mt</sub>_ is a martingale and _<sub>f</sub>_ (_<sub>.</sub>_) is a convex function. From Jensen’s inequality,

E_<sub>s</sub>_ \[_f_ (_M<sub>t</sub>_)\] _≥ f_ (E_<sub>s</sub>_ \[_M<sub>t</sub>_\]) = _f_ (_M<sub>s</sub>_)_._

Hence _<sub>f</sub>_ (_<sub>Mt</sub>_) is a submartingale.

##### Solution 2.2

From Itˆo’s lemma,

d_U_

_._

Which yields <sup>d</sup>_U<sup>U</sup>_ \= d_x_ \+  (d_x_)<sup>2</sup> \= _<sub>µ</sub>_ \+ _<sup>σ</sup>_2<sup>2 !</sup> d_t_ \+ _σ_ d_W_(_t_)_._

Similarly

d_V_

_._

Hence

<sup>d</sup>_V<sup>V</sup>_ \= <sup>1</sup>_t_ \+ _µ_ \+ _<sup>σ</sup>_2<sup>2 !</sup> d_t_ \+ _σ_ d_W_(_t_)_._

##### Solution 2.3

The application of Itˆo’s lemma yields

d_FF_ \= _−x_2 + _µx_<sub>1</sub>1 _− tµ_2 + _t_22_σ_22 _− xt_1 _σ_1_σ_2_ρ_!d_t_

+_σ_1 d_W_1_t − tσ_2 d_W_2_t. x_<sub>1</sub>

##### Solution 2.4

1.  From Itˆo’s lemma, we obtain

<sup>d</sup>_<sup>S</sup>_(<sup>(</sup>_t_)_<sup>t</sup>_<sup>)</sup> \= (_α_ \+ _β_ \+ _ρσv_) d_t_ \+ _σ_ d_W_(_t_) + _v_ d_Z_(_t_). _S_

Note that _<sub>σW</sub>_(_<sub>t</sub>_) + _<sub>vZ</sub>_(_<sub>t</sub>_) is a linear combination of Gaussian, centered processes. It is therefore a Gaussian, centered process. Its variance is

_σ_<sup>2</sup> \+ _v_<sup>2</sup> \+ 2_ρσvt._

Consequently, _<sub>S</sub>_(_<sub>t</sub>_) is a GBM with drift _<sub>α</sub>_ \+ _<sub>β</sub>_ \+ _<sub>ρσv</sub>_ and volatility <sup>p</sup>_<sub>σ</sub>_<sup>2</sup> ~~\+~~ _<sub>v</sub>_<sup>2</sup> ~~\+ 2~~_<sub>ρσv</sub>_.

1.  From Itˆo’s lemma, we obtain

d_<sup>Ut</sup>_ \= _α − β_ \+ _v_<sup>2</sup> _− ρσv_ d_t_ \+ _σ_ d_W_(_t_) _− v_ d_Z_(_t_).

_U<sub>t</sub>_

Again, _<sub>σW</sub>_(_<sub>t</sub>_) _<sub>− vZ</sub>_(_<sub>t</sub>_) is a linear combination of Gaussian, centered processes. It is therefore a Gaussian, centered process with variance

_σ_<sup>2</sup> \+ _v_<sup>2</sup> _−_ 2_ρσvt._

Consequently, _U<sub>t</sub>_ is a GBM with drift _α − <sub>β</sub>_ \+ _v_<sup>2</sup> _− <sub>ρσv</sub>_ and volatility <sup>p</sup>_<sub>σ</sub>_<sup>2</sup> \+ _v_<sup>2</sup> _−_ 2_ρσv_.

1.  In the ordinary least square regression model, the slope coefficient is given by

Cov d_XX_((_t_)_t_)_,_ d_YY_((_tt_))

d_X_(_t_) _._ Var _<sub>X</sub>_<sub>(</sub>_<sub>t</sub>_<sub>)</sub>

Note that

Cov <sup>d</sup>_X<sup>X</sup>_(<sup>(</sup>_<sub>t</sub>_)_<sup>t</sup>_<sup>)</sup>_<sub>,</sub>_ <sup>d</sup>_<sub>Y</sub><sup>Y</sup>_(<sup>(</sup>_<sub>t</sub><sup>t</sup>_)<sup>)</sup> \= Cov (_σ_ d_W_(_t_)_,v_ d_Z_(_t_)) = _σvρ_d_t._

Which yields

Cov d_XX_((_tt_))_,_ d_YY_((_tt_)) _ρv_

d_X_(_t_) \= _σ <sub>.</sub>_

Var _<sub>X</sub>_<sub>(</sub>_<sub>t</sub>_<sub>)</sub>

The constant is given by

<sup>1</sup> E 1 Cov d_X_(_t_) d_Y_ (_t_) E d ( <sup>)</sup> \=

<sup>d</sup>_Y_ <sup>(</sup>_t_) _X_(_t_) _, Y_ (_t_) _X t_ _αρv_

_dt Y_ (_t_) _− dt_ Var d_X_(_t_) _X_(_t_) _β − σ ._

_X_(_t_)

In the univariate regression, the _<sub>R</sub>_<sup>2</sup> coefficient is the squared correlation between <sup>d</sup>_<sub>X</sub><sup>X</sup>_<sub>(</sub><sup>(</sup>_<sub>t</sub><sup>t</sup>_<sub>)</sub><sup>)</sup> and <sup>d</sup>_<sub>Y</sub><sup>Y</sup>_<sub>(</sub><sup>(</sup>_<sub>t</sub>_<sub>)</sub>_<sup>t</sup>_<sup>)</sup>.

Thus

_R_<sup>2</sup> \= _ρ_<sup>2</sup>_._

**Chapter 3**

# The Black-Merton-Scholes model

The model developed by Black and Scholes (1973) and Merton (1973) offers closed-form solutions for pricing European options. It relies on perfect and arbitrage-free markets and the following price dynamics for the UA under the historical probability measure

<sup>d</sup>_<sup>S</sup>_(<sup>(</sup>_t<sup>t</sup>_)<sup>)</sup> \= (_µ <sub>− y</sub>_) d_t_ \+ _σ_ d_W_(_t_)_,_

_S_

where _<sub>µ</sub>_ stands for the instantaneous return, _<sub>y</sub>_ is the continuous dividend yield, _<sub>σ</sub>_ is the UA return volatility, and _<sub>{W</sub>_(_<sub>t</sub>_)_<sub>}t≥</sub>_<sub>0</sub> is a standard Brownian motion. In other words, the market price of the UA is assumed to follow a geometric Brownian motion with drift _<sub>µ − y</sub>_ and diffusion coefficient _<sub>σ</sub>_.

In the next two sections we solve for the pricing of European options using the PDE approach first, and then the martingale approach. We recall from the Feynman-Kac theorem that these two approaches are equivalent.

## 3.1 Solving the PDE

Without any loss in generality, we start with pricing the European call. Using the same arbitrage argument as in the former chapter, the European call premium satisfies

_∂c_( ) _∂c_(_t,T,K ∂_<sup>2</sup> (_<sub>t,T,K</sub>_)_<sub>,</sub>_ (3.1)

with boundary condition

_c_(_T,T,K_) = max(_S_(_T_) _− K_;0)_._

In their original article, Black and Scholes (1973) use several changes of variables to simplify the PDE into the heat equation that is well known by physicists. They obtain the following result.

**Proposition 3.1** _Under the assumptions of the Black-Merton-Scholes (BMS) model, the premium of the European call is given by_

_c_(0_,T,K_) = _S_(0)_e<sup>−yT</sup>_ Φ(_d_<sub>1</sub>) _− Ke<sup>−rT</sup>_ Φ(_d_<sub>2</sub>)_,_ (3.2)

65

_T d_<sub>1</sub> \= _√ ,_

_σ_

_T_

_√_

_d_<sub>2</sub> \= _d_<sub>1</sub> _− σ T,_

_and_ Φ(_<sub>.</sub>_) _stands for the standard normal cumulative distribution function._

The proposition can be verified by (i) using the fact, as mentioned in Section 1.3, that _<sub>c</sub>_(_<sub>t,T,K</sub>_) = _c_(0_<sub>,T</sub> − <sub>t,K</sub> |<sub>S</sub>_ \= _<sub>S</sub>_(_<sub>t</sub>_)), (ii) using Equation (3.2) to compute the partial derivatives of _<sub>c</sub>_(_<sub>t,T,K</sub>_), (iii) plugging them into the left-hand side of PDE (3.1) and checking that it is equal to the right-hand side. The function Φ(_<sub>.</sub>_) is defined by

Z _x_ d_u._

2_π −∞_

It is not known explicitly, however it is a common built-in function in most computational softwares and programming languages. These functions typically make use of polynomial approximations whose accuracy increases with the degree of the polynomial.<sup>1</sup>

The premium for the European put is obtained from the put-call parity, which yields (remember that

Φ(_−<sub>x</sub>_) = 1 _−_ Φ(_<sub>x</sub>_))

_p_(0_,T,K_) = _Ke<sup>−rT</sup>_ Φ(_−d_<sub>2</sub>) _− Se<sup>−yT</sup>_ Φ(_−d_<sub>1</sub>)_._ (3.3)

Again, _p_(_t,T,K_) = _p_(0_,T − t,K |S_ \= _S_(_t_)).

## 3.2 The martingale approach

We now solve for the premium of the European call using the martingale approach. When an analytical solution exists, the martingale approach method turns out to be a fast and effective pricing method as it only involves the computation of an expectation.

Using the fundamental martingale pricing property from the AoA and denoting Q the equivalent martingale measure,

_c_(0_,T,K_) = E<sup>Qh</sup>_e<sup>−rT</sup>_ max(_S_(_T_) _− K_;0)<sup>i</sup>

\= EQh_e−rT_ (_S_(_T_) _− K_)1_S_(_T_)_≥K_i_,_

where the indicator function 1_<sub>ω</sub>_ equals 1 if event _<sub>ω</sub>_ is true and 0 otherwise. Which yields

_c_(0_,T,K_) = _e<sup>−rT</sup>_ E<sup>Qh</sup>_S_(_T_)1_<sub>S</sub>_<sub>(</sub>_<sub>T</sub>_<sub>)</sub>_<sub>≥K</sub>_<sup>i</sup> _− Ke<sup>−rT</sup>_ Q(_S_(_T_) _≥ K_)_._ (3.4)

<sup>1</sup>Below is polynomial approximation of order 5 that yields an accurate approximation for Φ(_._) up to the sixth decimal

Φ(_x_) _≈_ 1 _− ϕ_(_x_) _a_<sub>1</sub>_k_ \+ _a_<sub>2</sub>_k_<sup>2</sup> \+ _a_<sub>3</sub>_k_<sup>3</sup> \+ _a_<sub>4</sub>_k_<sup>4</sup> \+ _a_<sub>5</sub>_k_<sup>5</sup> for _x ≥_ 0_,_

where _ϕ_(_._) is the standard normal density function

_,_

and

1

_k_ \= _,_

1 + _γx_

_γ_ \= 0_._2316419 _a_<sub>1</sub> \= 0_._319381530 _a_<sub>2</sub> \= _−_0_._356563782 _a_<sub>3</sub> \= 1_._781477937 _a_<sub>4</sub> \= _−_1_._821255978 _a_<sub>5</sub> \= 1_._330274429_._

Under Q, the market price of the UA is driven by the following geometric Brownian motion

<sup>d</sup>_<sup>S</sup>_(<sup>(</sup>_t_)_<sup>t</sup>_<sup>)</sup> \= (_r <sub>− y</sub>_) d_t_ \+ _σ_ d_W_(_t_)_,_

_S_

and can be written as

" _S_(_T_) = _S_ exp _r._

Therefore the event _<sub>S</sub>_(_<sub>T</sub>_) _<sub>≥ K</sub>_ can also be characterized as

" _S_ exp _rK,_

or, alternatively,

_W_(_T_) _≥_ 1 "ln _K −_ _r − y − σ_22 !_T_#_. σ S_

From the properties of the Brownian motion, the variable _<sub>W</sub>_(_<sub>T</sub>_) is normally distributed with mean zero and variance _<sub>T</sub>_. Consequently, the event _<sub>S</sub>_(_<sub>T</sub>_) _<sub>≥ K</sub>_ has the same probability as the event

1 "ln _K −_ _r − y − σ_2 ! # _ε ≥ σ√T S_ 2 _T ._

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| Thus |     |     |     |     |     |
|     | Q(_S_(_T_) _≥ K_) | \=  | 1<br><br>Q _ε ≥ √_<br><br>_σ T_ | " 2 !<br><br>_K σ_<br><br>ln _− r − y −_ 2 _T_<br><br>_S_ | #!<br><br>_,_ |

" _K_ _σ_2 ! #!

\=

1

_−_

Q

_ε_

_≤_

1

_σ_

_√_

_T_ ln _S − r − y −_ 2 _T ,_

|     |     |     |
| --- | --- | --- |
|     |     | _σ T <sup>S</sup>_ 2 |
| \=  | Φ   | 1 " _S_ _σ_2 ! #!<br><br>_√_ <sup>ln +</sup> _r − y − T ,_ |

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
|     | _σ T_ | _K_ | 2   |     |
| Furthermore, | \= Φ(_d_<sub>2</sub>)_._ |     |     | (3.5) |
|     | EQh_S_(_T_)1_S_(_T_)_≥K_ | i = Z | _S_(_T_)_ϕ_(_ε_) d_ε._ |     |

\= 1 _−_ Φ _√_1 "ln _K −_ _r − y − σ_2 !_T_#!_,_

_S_(_T_)_≥K_

Which yields, from the characterization of the event _<sub>S</sub>_(_<sub>T</sub>_) _<sub>≥ K</sub>_ and the value of _<sub>S</sub>_(_<sub>T</sub>_),

 Z _∞_ !

EQh_S_(_T_)1_S_(_T_)_≥K_i =d_ε,_

!

\= _SeTε_d_ε._

We proceed to the following change of variable

|     |     |     |     |
| --- | --- | --- | --- |
| _Y_ | \=  | _ε − σ_ | _√_<br><br>_T,_ |
| _dY_ and obtain, after simplifications | \=  | d_ε,_ |     |

Z _∞_2 !

1

_√_

exp

_−_

_Y_

2

EQh_S_(_T_)1_S_(_T_)_≥K_i = _Se_(_r−y_)_T √dY,_

_−d_<sub>2</sub>_−σ T_ ~~2~~_π_ 2 !

\= _Se dY,_

 = _Se,_

\= _Se_(_r−y_)_T_ Φ(_d_1)_._ (3.6) Combining results (3.5) and (3.6) and plugging them into (3.4) leads to the analytical formula for the premium of the European call shown in the Proposition.

Note that equation (3.5) allows to interpret Φ(_<sub>d</sub>_<sub>2</sub>) as the probability, under the EMM, that the call ends up in-the-money. Regarding _<sub>e</sub><sup>−yT</sup>_ Φ(_<sub>d</sub>_<sub>1</sub>), we can interpret this factor as the partial derivative of the call premium with respect to the UA price. Indeed, _∂c_(0

_,_

_,_

\= _e−yT_ Φ(_d_1) + 1_~~√~~_ h_Se−yT ϕ_(_d_1) _− Ke−rT ϕ_(_d_2)i_,_

_Sσ T_

\= _e−yT_ Φ(_d_1)_._

The last equality stems from the fact that _<sub>Se</sub><sup>−yT</sup> <sub>ϕ</sub>_(_<sub>d</sub>_<sub>1</sub>) = _<sub>Ke</sub><sup>−rT</sup> <sub>ϕ</sub>_(_<sub>d</sub>_<sub>2</sub>), which can be established, after cumbersome calculations, using the definitions of _<sub>d</sub>_<sub>1</sub> and _<sub>d</sub>_<sub>2</sub>. The partial derivative of the option premium with respect to the UA price is commonly referred to as the option _delta_. We noticed in the previous chapter that it is the quantity of UA held in the locally riskless arbitrage portfolio. In Chapter 4, we will discuss the delta in greater detail for the risk management of derivatives.

## 3.3 Digital options

Digital options (or binary options) are European-style derivatives written on a certain quantity of UA (_asset-or-nothing_ options) or on some fixed monetary amount (_cash-or-nothing_ options). The terminal payoffs of the cash-or-nothing call and put are:

_cash_ (_T,T,K,M_) = <sup>(</sup> _M_0 otherwiseif _S_ (_T_) _\> K ,_

_cdig_

_pcashdig_ (_T,T,K,M_) = ( _M_0 otherwiseif _S_ (_T_) _< K ,_

while the terminal payoffs of the asset-or-nothing call and put are:

_cassetdig_ (_T,T,K,λ_) = ( _λS_0 (_T_) ifotherwise_S_ (_T_) _\> K ,_

_passetdig_ (_T,T,K,λ_) = ( _λS_0 (_T_) ifotherwise_S_ (_T_) _< K ._

Digital options can be viewed as building blocks used to construct the payoff of European options. Indeed, in the AoA,

_c_(_t,T,K_) = _c<sup>asset</sup><sub>dig</sub>_ (_t,T,K,_1) _− c<sup>cash</sup><sub>dig</sub>_ (_t,T,K,K_)_, p_(_t,T,K_) = _p<sup>cash</sup><sub>dig</sub>_ (_t,T,K,K_) _− p<sup>asset</sup><sub>dig</sub>_ (_t,T,K,_1)_._

The valuation of digital options in the BMS framework is straightforward given earlier calculations:

|     |     |
| --- | --- |
| _ccashdig_ (_t,T,K,M_) = _Me−r_(_T−t_)Φ(_d_2)_,_ | _cassetdig_ (_t,T,K,λ_) = _λS_(_t_)_e−y_(_T−t_)Φ(_d_1)_,_ |
| _pcashdig_ (_t,T,K,M_) = _Me−r_(_T−t_)Φ(_−d_2)_,_ | _passetdig_ (_t,T,K,λ_) = _λS_(_t_)_e−y_(_T−t_)Φ(_−d_1)_._ |

## 3.4 Perpetual options

A perpetual option can be exercised at any time without any restricting deadline. It is therefore equivalent to an American option with infinite maturity. These options can be valued analytically in the BMS framework.

Let _<sub>P</sub>_(_<sub>t,∞,K</sub>_) denote the premium of the perpetual put with UA price process _<sub>S</sub>_ and strike price _K_. Since the perpetual put is infinitely lived, its value is not affected by the mere passage of time, i.e.

_∂P_(_<sub>t,</sub>∞<sub>,K</sub>_)_<sub>/∂t</sub>_ \= 0. It follows that in the AoA, the premium _<sub>P</sub>_(_<sub>t,</sub>∞<sub>,K</sub>_) satisfies the Ordinary Differential

Equation (ODE)

_._

The general solution is

_P_(_t,∞,K_) = _a_<sub>1</sub>_S<sup>αp</sup>_(_t_) + _a_<sub>2</sub>_S<sup>αc</sup>_(_t_)_,_

with _<sub>a</sub>_<sub>1</sub> and _<sub>a</sub>_<sub>2</sub> two constants to be determined, and _<sub>αp</sub>_ and _<sub>αc</sub>_ the two roots of the quadratic equation

|     |     |
| --- | --- |
| which yields | _σ_2<br><br>2 _α_(_α −_ 1) + (_r − y_)_α − r_ \= 0_,_ |

_α<sub>p</sub>_ \= _−σ_1 _r −σ y − σ_2 + s

_r_

_−_

_y_

_σ_

_−_

_σ_

2

2

+2

_r_





_<_

0

_,_

_r_

_−_

_y_

_−_

2

+2

_r_





_\>_

0

_._

_α<sub>c</sub>_ \= _−σ_1 _r − y − σ_2 _−_ s _<sub>σ</sub> σ_2

_<sub>σ</sub>_

The boundary conditions associated with the perpetual put are

lim _P_(_t,∞,K_) = 0_,_

_S→∞_

_P_ (_t,∞,K |S_(_t_) = _S<sup>∗</sup>_) = _K − S<sup>∗</sup>,_

where _<sub>S</sub><sup>∗</sup>_ denotes the optimal exercise threshold.

From the first condition we infer that _<sub>a</sub>_<sub>2</sub> \= 0. The second condition then yields

_a_1_S∗αp_ \= _K − S∗,_

and the premium of the perpetual put is given by

_αp_

_P <sub>.</sub>_ (3.7)

_S_

Equation (3.7) can be easily interpreted if we notice that the present value of $1 received the first time that _<sub>S</sub>_(_<sub>t</sub>_) reaches the lower level _<sub>S</sub><sup>∗</sup>_ is (_<sub>S</sub>_(_<sub>t</sub>_)_<sub>/S</sub><sup>∗</sup>_)_<sup>αp</sup>_ (this is left as an exercise). Put differently, the quantity (_<sub>S</sub>_(_<sub>t</sub>_)_<sub>/S</sub><sup>∗</sup>_)_<sup>αp</sup>_ is the Arrow-Debreu price of the security paying $1 contingent on the exercise of the perpetual put. It is therefore the relevant discounting factor for the perpetual put payoff _<sub>K − S</sub><sup>∗</sup>_.

The optimal exercise threshold maximizes the value of the perpetual put and can be obtained from the first order condition

_S∗_ \= _α<sub>p</sub>α−p_ 1_K._

Hence !_αp_

_P_(_t,∞,K_) = 1 _<sub>−</sub>K<sub>α</sub>p α<sup>p</sup><sub>α</sub>−p_ 1 _S<sub>K</sub>_(_t_) _._

## 3.5 Historical and implied volatilities

As can be seen from equation (3.2), the European option premium is a function of a set of observable parameters: The price of the UA (_<sub>S</sub>_), the terms of the contract (_<sub>K</sub>_ and _<sub>T</sub>_), the risk-free rate (_<sub>r</sub>_) and the dividend yield (_<sub>y</sub>_). It is also a strictly increasing function of one non-observable parameter, namely the volatility _<sub>σ</sub>_. Given a value set to all observable inputs, the BMS option formula therefore establishes a one-to-one relation (i.e. a bijection) between the option premium and the volatility parameter _<sub>σ</sub>_.

Measuring and forecasting volatility is the topic of countless articles and handbook chapters. Whereas estimators for _<sub>σ</sub>_ can arguably be very accurate depending on the data at hand, volatility remains intrinsically unobservable. We will revisit the topic in more detail later in this book. At this point, we consider the simplest approach from each of two broad families of estimators.

One way is to compute a historical volatility based on a time series of past UA returns. Let _{<sub>Sn</sub>}<sub>n</sub>_<sub>\=0</sub>_<sub>,...,N</sub>_ denote a collection of _<sub>N</sub>_ +1 daily prices of the UA (typically end-of-day closing prices). The time series of

_N_ log-returns _{R<sub>n</sub>}<sub>n</sub>_<sub>\=1</sub>_<sub>,...,N</sub>_ can be computed as

_R<sub>n</sub>_ \= ln _<sup>Sn</sup> ,_ for all _n_ \= 1_,...,N._

_Sn−_1

An estimate for the historical asset return daily volatility over the sample period is given by

v u

_σ_<sup>b</sup>_d_ \= ut_N −_ 1 _n_\=1 _Rn − R N −_ 1 _n_\=1 _n_2 _N −_ 1_R ,_

1

_N_

X

2

\=

v

u

u

t

1

_N_

X

_R_

_−_

_N_

2

where

_R_ \= 1 X_N Rn_

_N_

_n_\=1 is the average log-return over the sample period.

Several empirical studies (Fama (1965), French (1980)) have shown that the variance of asset returns essentially comes from the trading activity during days when the financial market is open. As a consequence, the daily volatility (_<sub>σ</sub>_<sub>b</sub>_d_) is converted into the annual volatility (_<sub>σ</sub>_<sub>b</sub>_y_) by using the number of trading days during the year (_<sub>Nd</sub>_), that is,<sup><sup>[\[4\]](#footnote-4)</sup></sup>

_σy_ \= _σ_<sub>b</sub>_d_<sup>p</sup>_N<sub>d</sub>,_ (3.8) <sub>b</sub> where in practice _<sub>Nd</sub> ≃_ 252 for stock, bond, or commodity markets, and _<sub>Nd</sub>_ \= 365 for the foreign exchange market.

Another approach is to exploit the aforementioned bijection between volatility and option prices. For instance, since the BMS formula for European calls and puts is strictly increasing in _<sub>σ</sub>_, it can be inverted around the market price of the option to obtain to sole value of _<sub>σ</sub>_ consistent with that price. This is referred to as the _implied volatility_ of the option. Specifically, let _<sub>g</sub><sup>obs</sup>_ be the market premium of a European option and _<sub>fBMS</sub>_ (_<sub>.</sub>_) denote the BMS valuation formula for that derivative. Given all other parameters for the function _<sub>fBMS</sub>_ (_<sub>.</sub>_), there implicitly exists an implied volatility _<sub>σ</sub><sup>imp</sup>_ such that

_f<sub>BMS</sub> σimp,._ \= _gobs._

The implied volatility of the derivative can therefore be retrieved as

_σimp_ \= _<sup>f</sup><sub>BMS</sub>−_1 _gobs,.._

Historical and implied volatilities tend to be quite different. An important consideration (among many others) is that the estimation of historical volatility relies on past information only, whereas the implied volatility is a forward-looking metric that reflects market anticipations about future UA price variations.

As an example, consider a company announcing now that it will make an important business decision in _<sub>τ</sub>_ trading days. Right after the announcement, the implied volatility is likely to rise, as the market recognizes the uncertainty surrounding the business decision that will not be resolved before _<sub>τ</sub>_ trading days. The historical volatility, by contrast, will be little affected, since its calculation is based for the most part on trading days preceding the announcement. Once the _<sub>τ</sub>_ trading days have passed and the business decision is known to the market, there is no more major uncertainty ahead and the implied volatility will likely decrease. However, the historical volatility will rise because its calculation will be impacted by the volatile days between now and the next _<sub>τ</sub>_ trading days.

## 3.6 The market price of risk

The goal of this section is to characterize the risk / return relationship for derivatives in the BMS framework. In other words, we examine the link that exists in the absence of arbitrage between the drift and the diffusion coefficient for derivatives returns.

Let us apply Itˆo’s lemma on the value of a derivative _<sub>g</sub>_<sub>1</sub> (_<sub>S,t</sub>_) written on _<sub>S</sub>_.

_dg__σS_ d_W_(_t_)_._

Setting

!

_,_

_σS,_

we can write that

_<sup>dg</sup>_<sup>1</sup> \= _α_<sub>1</sub> d_t_ \+ _β_<sub>1</sub> d_W_(_t_)_. g_<sub>1</sub>

A similar application of Itˆo’s lemma on the value of another derivative _<sub>g</sub>_<sub>2</sub> (_<sub>S,t</sub>_) written on _<sub>S</sub>_ yields

_<sup>dg</sup>_<sup>2</sup> \= _α_<sub>2</sub> d_t_ \+ _β_<sub>2</sub> d_W_(_t_)_, g_<sub>2</sub>

where the drift _<sub>α</sub>_<sub>2</sub> and the diffusion coefficient _<sub>β</sub>_<sub>2</sub> have analogous definitions.

Now consider the self-financing portfolio _<sub>P</sub>_ containing the two derivatives. For _<sub>P</sub>_ to be locally riskless, we need to buy the quantity _<sub>β</sub>_<sub>2</sub>_<sub>g</sub>_<sub>2</sub> of the first derivative and to sell the quantity _<sub>β</sub>_<sub>1</sub>_<sub>g</sub>_<sub>1</sub> of the second derivative.

With such a portfolio composition, we obtain

_dP_ \= _β_<sub>2</sub>_g_<sub>2</sub>_dg_<sub>1</sub> _− β_<sub>1</sub>_g_<sub>1</sub>_dg_<sub>2</sub>

\= (_β_2_g_2_α_1_g_1 _− β_1_g_1_α_2_g_2) d_t._

Under the AoA, this locally riskless portfolio must earn the risk-free rate, i.e.

_dP_ \= _rP_ d_t,_

which yields, after rearranging

_α_<sup>1</sup> _− r_ \= _α_<sup>2</sup> _− r<sub>.</sub>_ (3.9) _β_1 _β_2

Equation (3.9) involves the market price of risk, that is, the ratio of the risk premium _<sub>αi − r</sub>_, _<sub>i</sub>_ \= 1_<sub>,</sub>_2, over the quantity of risk (measured by volatility) _<sub>βi</sub>_, _<sub>i</sub>_ \= 1_<sub>,</sub>_2\. Notice that equation (3.9) is valid for any arbitrary pair of derivatives _<sub>g</sub>_<sub>1</sub> and _<sub>g</sub>_<sub>2</sub>. It therefore holds for all derivatives written on _<sub>S</sub>_. Thus, the ratio of excess return over volatility, known as the Sharpe ratio, is a constant _<sub>λ</sub>_ called the market price of risk.

Let us rewrite the formula for the market price of risk using the definitions of _<sub>α</sub>_ and _<sub>β</sub>_ for any arbitrary derivative _<sub>g</sub>_:

_λ_ \= "_g_1 _∂g∂t_ \+ _∂S∂g_ (_µ − y_)_S_ \+ 21 _∂S∂_2_g_2 _σ_2_S_2! _− r_#_/g_1 _∂S∂g σS,_

which yields

 _rg._ (3.10)

Recall that the fundamental PDE under the AoA requires that

 _rg._

Hence it must be that

_µ − y − λσ_ \= _r − y,_

or, equivalently,

_<sub>λ</sub>_ \= _µ − r<sub>.</sub>_

_σ_

We synthesize our findings under the following proposition.

**Proposition 3.2** _Suppose there exists <sub>n</sub> derivatives written on the same UA._

1.  _In the BMS framework, the market price of risk is the same across all <sub>n</sub> derivatives. It is the constant λ defined by_

_λ_ \= _<sup>αi − r</sup>,∀i_ \= 1_,...,n,_

_β<sub>i</sub>_

_where <sub>αi</sub> and <sub>βi</sub> are respectively the drift and the diffusion coefficient of the stochastic differential equation for the return on derivative <sub>gi</sub>._

1.  _In the BMS framework, the market price of risk is the same across all derivatives written on a givenUA, and it is equal to the market price of risk of the UA, that is_

_µ − r_ \= _αi − r,∀i_ \= 1_,...,n. σ β<sub>i</sub>_

One way to illustrate the intuition beneath that proposition is by considering a set of options written on the same UA but with different moneyness. Far-from-the-money options exhibit a low risk / return profile. Their expected return and volatility are low because their value is likely to stay close to their intrinsic value. By contrast, near-the-money options exhibit a high risk / return profile for the opposite reason. The proposition states that these risk / return profiles vary across option moneyness in such a way that the market price of risk remains constant.

The two parts of the proposition hold under the BMS framework where the UA is assumed to be traded on a financial market. Note, however, that only the second part of the proposition actually requires that assumption. The first part (all derivatives have the same, constant market price of risk) holds when the UA price dynamics are driven by a geometric Brownian motion but the UA need not be traded. Indeed, to derive the first part of the proposition, we relied on an arbitrage portfolio with positions on derivatives but no position in the UA. Only the second part of the proposition invokes the fundamental PDE which is derived from an arbitrage portfolio containing the UA.

As a consequence, if we use a geometric Brownian motion to model the dynamics of an untraded UA (like temperatures or precipitations underlying weather derivatives for example), then all derivatives have the same, constant market price of risk (first part of the proposition). But that constant market price of risk is different from the market price of risk of the UA (second part of the proposition does not hold). This difference can be interpreted as a risk premium for trading derivatives written on an untraded UA.

## 3.7 Specific underlying assets

This section discusses how to adjust the BMS option pricing formula when the UA is a forward contract or when it pays discrete dividends.

### 3.7.1 Options on forwards

Under the BMS framework, the risk-neutral dynamics of the spot price of the UA is given by

<sup>d</sup>_<sup>S</sup>_(<sup>(</sup>_t<sup>t</sup>_)<sup>)</sup> \= (_r <sub>− y</sub>_) d_t_ \+ _σ_ d_Z_(_t_)_. S_

We can use the cash and carry relation

_f_ (_t,T_) = _S_(_t_)exp\[(_r − y_)(_T − t_)\]_,_

and apply Itˆo’s lemma to the forward price to obtain

_df_ (_t,T_) = _−_(_r − y_)_S_(_t_)exp\[(_r − y_)(_T − t_)\] d_t_ \+ exp\[(_r − y_)(_T − t_)\] d_S_(_t_)_._

Which yields _dff_ ((_t,Tt,T_)) = _−_(_r − <sup>y</sup>_) d_t_ \+ d_SS_((_tt_)) = _σ_ d_Z_(_t_)_,_

or, equivalently,

_f_ (_t,T_) = _f_ (0_,T_)exp _<sub>σZ</sub>_(_t_) _− <sup>σ</sup>_2<sup>2</sup> _<sub>t</sub>_<sup>!</sup>_<sub>.</sub>_

We conclude that the forward price is a martingale under the risk-neutral probability measure. Put differently, the forward price is an unbiased predictor of the future spot price under Q.

The premium of the European call on the forward is therefore obtained as a special case where the risk-neutral drift of the UA is set to zero. The following result was initially provided by Black (1976).

**Proposition 3.3** _Under the BMS framework, the premium of the European call with expiration date <sub>T</sub> written on the forward contract with delivery date <sub>θ ≥ T</sub> is given by_

_c_(_t,T,K_) = _e<sup>−r</sup>_<sup>(</sup>_<sup>T−t</sup>_<sup>)</sup> \[_f_(_t,θ_)Φ(_d_<sub>1</sub>) _− K_Φ(_d_<sub>2</sub>)\]_,_

_where_

_d_ _√ ,_

_σ T − t √ d_<sub>2</sub> \= _d_<sub>1</sub> _− σ T − t._

_The premium of the put is obtained from put-call parity._

### 3.7.2 Underlying asset with discrete dividends

Consider an UA (typically the stock of a company) that pays discrete dividends. For pricing derivatives, only the dividends paid before maturity _<sub>T</sub>_ matter. Let _<sub>N</sub>_ denote the number of dividends paid before _<sub>T</sub>_, and _<sub>δ</sub>_ (_<sub>tn</sub>_) the dividend amounts due at dates _<sub>tn</sub> ∈_ (_<sub>t,T</sub>_), _<sub>n</sub>_ \= 1_<sub>,...,N</sub>_. Companies usually pay dividends at a quarterly or semi-annual frequency. For most exchange-traded derivatives, the maturity is below one year. Therefore in practice, _<sub>N</sub>_ barely exceeds 2 or 3.

We assume the _<sub>tn</sub>_ and the _<sub>δ</sub>_ (_<sub>tn</sub>_) are known with certainty. The payment of a dividend triggers a stock price drop so that the UA price right after date _<sub>tn</sub>_ can be written as

_S t_+_n_ \= _S t−n_ _− δ_ (_tn_)_._

Elton and Gruber (1970) prove by arbitrage that the price drop on a dividend payment date is in fact affected by the differential taxation between dividends and capital gains. Specifically,

_S t−n_ _− S t_+_n_ \= 11 _−− ττdg δ_ (_tn_)_,_

where _<sub>τd</sub>_ and _<sub>τg</sub>_ denote the tax rates on dividends and on capital gains, respectively.

In a study on the Chicago Board of Exchange, Barone-Adesi and Whaley (1986) document that the price drop on a dividend payment date is not significantly different from the dividend amount. Ultimately, whether the stock price drop equals the dividend amount or only a fraction of it remains an empirical issue.

The BMS pricing formulas for European options are still the same, except that the current value of the UA is reduced by the sum of all discounted price drops expected before option maturity.

**Proposition 3.4** _Under the BMS framework, the premium of the European call written on an UA paying N discrete dividends <sub>δ</sub>_ (_<sub>tn</sub>_)_, at dates <sub>tn</sub> ∈_ (_<sub>t,T</sub>_)_<sub>,n</sub>_ \= 1_<sub>,...,N</sub>, is given by (assuming the stock price drops are equal to a fraction <sub>α</sub> of the dividend amounts)_

_c_(_t,T,K_) = _S_<sub>b</sub>(_t_)Φ(_d_<sub>1</sub>) _− Ke<sup>−r</sup>_<sup>(</sup>_<sup>T−t</sup>_<sup>)</sup>Φ(_d_<sub>2</sub>)_,_

_with_

_d_<sub>1</sub> \= _,_

ln

b

_S_

(

_t_

)

_K_

+

_r_

+

_σ_

2

2

(

_T_

_−_

_t_

)

_σ_

_√_

_T_

_−_

_t_

_√_

_d_<sub>2</sub> \= _d_<sub>1</sub> _− σ T − t,_

_and_

_N_

_S_b(_t_) = _S_(_t_) _−_ X _αδ_ (_tn_)_e−r_(_tn−t_)_._

_n_\=1

_The premium of the put is obtained from put-call parity._

## 3.8 American options

Because of their early exercise feature, (finite-maturity) American options cannot be valued analytically (even under the BMS framework) except for the specific case of the American call written on a spot UA with no dividend. One must therefore resort to numerical methods (such as trees, grids or simulations that will be studied in the next chapters). Under the BMS framework, there exist quasi-analytical methods to value American options, which represent relatively fast and accurate alternatives to numerical methods. We will examine two of them in this section.

The first method, initiated by MacMillan (1986) and Barone-Adesi and Whaley (1987), consists in approximating the pricing problem by slightly modifying the original PDE. It yields a quasi-analytical solution in the sense that one must find the root of a non-linear equation. The second method, developed by Kim (1990), Jacka (1991) and Carr et al. (1992), proceeds with the integral representation of the exercise boundary. In this approach the determination of American option premiums requires numerical integration whose complexity can be lowered using approximations.

### 3.8.1 Quasi-analytical approximation

We present the Barone-Adesi and Whaley (1987) model that offers a fast, yet not very accurate solution.

Within a BMS framework, the premium of an American option _<sub>ga</sub>_ satisfies the fundamental PDE

_∂g_

_rg<sub>a</sub>,_

and so does the premium of the corresponding European option _<sub>ge</sub>_

 _rg<sub>e</sub>._

It follows that the early exercise premium _<sub>v</sub>_ \= _<sub>ga − ge</sub>_ also verifies the fundamental PDE

 _rv._

Let _<sub>α</sub>_ \= 2_<sub>r/σ</sub>_<sup>2</sup>, _<sub>β</sub>_ \= 2(_<sub>r</sub> − <sub>y</sub>_)_<sub>/σ</sub>_<sup>2</sup> and _<sub>τ</sub>_ \= _<sub>T</sub> − <sub>t</sub>_, the PDE followed by _<sub>v</sub>_ can be rewritten as

_α_ <sup>2</sup> \= _αv,_

_− v<sub>τ</sub>_ \+ _v<sub>S</sub>βS_ \+ _v<sub>SS</sub>S r_

where we use the compact notation _<sub>vx</sub>_ \= _<sub>∂v/∂x</sub>_.

The first key hypothesis of the model consists in assuming that _<sub>v</sub>_ can be written as

_v_ \= _h_(_τ_)_f_ (_S,h_)_._

The _<sub>h</sub>_ function depends on time only and therefore specifically accounts for the discount effect. By contrast, the _<sub>f</sub>_ function depends on both _<sub>S</sub>_ and _<sub>h</sub>_ and thus captures the speculation effect. Partial derivatives are

_v<sub>τ</sub>_ \= _h<sub>τ</sub>_ (_τ_)_f_ (_S,h_) + _h_(_τ_)_h<sub>τ</sub>_ (_τ_)_f<sub>h</sub>_ (_S,h_)_,_

_v<sub>S</sub>_ \= _h_(_τ_)_f<sub>S</sub>_ (_S,h_)_, v<sub>SS</sub>_ \= _h_(_τ_)_f<sub>SS</sub>_ (_S,h_)_._

The PDE followed by _<sub>v</sub>_ becomes, after dividing by _<sub>h</sub>_(_<sub>τ</sub>_) and factoring,

_−αf_ (_S,h_)1 + _<sup>h</sup>_ (_<sup>τ</sup>_) 1 + _<sup>h</sup>_(_<sup>τ</sup>_)_<sup>f</sup>_ (_<sup>S,h</sup>_) \+ _f<sub>S</sub>_ (_S,h_)_βS_ \+ _f<sub>SS</sub>_ (_S,h_)_S_<sup>2</sup> \= 0_. rhf_

The second key hypothesis is to consider a specific form for _<sub>h</sub>_(_<sub>τ</sub>_):

_h_(_τ_) = 1 _−_ exp(_−rτ_)_, h<sub>τ</sub>_ (_τ_) = _r_exp(_−rτ_) = _r_(1 _− h_(_τ_))_._

Under this assumption, the PDE followed by _<sub>v</sub>_ simplifies to

_h−_(_α<sub>τ</sub>_) \[_f_ (_S,h_) + (1 _− h_(_τ_))_h_(_τ_)_f<sub>h</sub>_ (_S,h_)\] + _f<sub>S</sub>_ (_S,h_)_βS_ \+ _f<sub>SS</sub>_ (_S,h_)_S_<sub>2</sub> \= 0_<sub>.</sub>_

The Barone-Adesi and Whaley (1987) approximation consists in neglecting the product (1 _<sub>− h</sub>_(_<sub>τ</sub>_))_<sub>h</sub>_(_<sub>τ</sub>_) in the PDE. This can be justified by noting that for options with very long maturities (_<sub>T → ∞,</sub>_ thus _<sub>h</sub>_(_<sub>τ</sub>_) _<sub>→</sub>_ 1), or very short maturities (_<sub>h</sub>_(_<sub>τ</sub>_) _<sub>→</sub>_ 0) the product (1 _<sub>− h</sub>_(_<sub>τ</sub>_))_<sub>h</sub>_(_<sub>τ</sub>_) indeed approaches to zero. Thanks to that approximation, the PDE becomes a second order ODE whose generic solution is given by

_f_ (_S_) = _a_1_Sγ_1 + _a_2_Sγ_2

where _<sub>a</sub>_<sub>1</sub> and _<sub>a</sub>_<sub>2</sub> are two arbitrary constants and _<sub>γ</sub>_<sub>1</sub> and _<sub>γ</sub>_<sub>2</sub> are the roots of the quadratic equation

_α γ_ (_γ −_ 1) + _βγ −_ (_<sub>τ</sub>_) = 0_, <sub>h</sub>_

that is:

_γ_<sub>1</sub> \= _−_(_β −_ 1) _−_ <sup>s</sup>(_β −_ 1)<sup>2</sup> \+ <sup>4</sup>(_<sup>α</sup><sub>τ</sub>_)<sup>!</sup> _<sub><</sub>_ 0_, <sub>h</sub>_

\=

_γ_2 _<sub>−</sub>_(_β −_ 1) + <sup>s</sup>(_β −_ 1)<sup>2</sup> \+ _h_<sup>4</sup>(_<sup>α</sup><sub>τ</sub>_)<sup>!</sup> _<sub>\></sub>_ 0_._

We now proceed to valuing the American call. The boundary condition lim _<sub>C</sub>_ (_<sub>t,T,K</sub>_) = 0 implies

_S_(_t_)_→_0 that _<sub>a</sub>_<sub>1</sub> \= 0. The American call premium is therefore of the form

_C_ (_t,T,K_) = _c_(_t,T,K_) + _h_(_τ_)_a_<sub>2</sub>_S<sup>γ</sup>_<sup>2</sup>_._

Let us introduce the threshold _<sub>S</sub><sup>∗</sup>_ above which the American call option should be exercised. That is:

_<sup>C</sup>_ (_<sup>t,T,K</sup>_) = ( _<sub>S</sub>c_((_t,T,Kt_) _<sub>−</sub> K_) + _h_(_τ_)_a_<sub>2</sub>_S<sup>γ</sup>_<sup>2</sup>(_t_) ifif _SS_((_tt_)) _<≥ SS∗<sup>∗</sup>,._

The two unknown parameters _<sub>a</sub>_<sub>2</sub> and _<sub>S</sub><sup>∗</sup>_ are obtained by applying the following two conditions. First, a _value-matching condition_ entails that when the UA is worth _<sub>S</sub><sup>∗</sup>_, the value of the American call must be equal to the exercise value, that is:

_S<sup>∗</sup> − K_ \= _c_(_t,T,K |S_ \= _S<sup>∗</sup>_) + _h_(_τ_)_a_<sub>2</sub>_S<sup>∗γ</sup>_<sup>2</sup>_._ Second, if the American option holder is indifferent between exercising and keeping the option alive at _S_ \= _<sub>S</sub><sup>∗</sup>_, it must be that the marginal continuation value is equal to the marginal exercise value (this equality in slopes is referred to as a _smooth-pasting condition_). In other words, the delta of the American call option is equal to 1 at _<sub>S</sub>_ \= _<sub>S</sub><sup>∗</sup>_, that is:

1 = _e−yτ_Φ(_d_1 (_S∗_)) + _h_(_τ_)_a_2_γ_2_S∗γ_2_−_1_,_

where

_d__._

The value-matching and smooth pasting conditions yield a system of two equations with two unknowns (_<sub>a</sub>_<sub>2</sub> and _<sub>S</sub><sup>∗</sup>_). Its resolution leads to the following formula for the American call premium.

**Proposition 3.5** _According to the Barone-Adesi and Whaley (1987) approximation, the value of the American call is given by_

_<sup>C</sup>_ (_<sup>t,T,K</sup>_) = ( _S_((_t,T,Kt_) _<sub>−</sub> K_) + _<sub>S</sub> <sup>γ</sup>_<sup>2</sup> _ifif SS_((_tt_))_≥<SS∗<sup>∗ ,</sup> c_

_<sup>where</sup> A_<sub>2</sub> \= _S∗_ _−y_(_T−t_)Φ(_d_<sub>1</sub> (_S∗_))_,_

1 _− e_

_γ_<sub>2</sub>

_and <sub>S</sub><sup>∗</sup> is the solution of the non-linear equation_

_S∗_ _−y_(_T−t_)Φ(_d_1(_S∗_))_._

_S∗ − K_ \= _c_(_t,T,K |S_ \= _S∗_) + 1 _− e γ_<sub>2</sub>

The determination of _<sub>S</sub><sup>∗</sup>_ presents no numerical difficulty as it can be shown that the non-linear equation above admits a unique root in _<sub>S</sub><sup>∗</sup>_ when _<sub>y ></sub>_ 0.

Valuing the American put option goes along very similar lines. The associated boundary condition lim _<sub>P</sub>_ (_<sub>t,T,K</sub>_) = 0 implies that _<sub>a</sub>_<sub>2</sub> \= 0. Hence

_S_(_t_)_→∞_

_P_(_t,T,K_) = _p_(_t,T,K_) + _h_(_τ_)_a_<sub>1</sub>_S<sup>γ</sup>_<sup>1</sup>(_t_)_._

Applying the value-matching and smooth pasting conditions yields the following proposition.

**Proposition 3.6** _According to the Barone-Adesi and Whaley (1987) approximation, the value of the Amer-_

_ican put is given by_

_P_(_t,T,K_) = _p_(_t,T,K_) + _A_1 _S∗∗γ_1

_if S<sup>∗∗</sup> ≥ S_(_t_) _if S<sup>∗∗</sup> < S_(_t_) _<sup>,</sup>_

_where_

_S<sub>∗∗</sub>_

_A_1 = _−_ 1 _− e−y_(_T−t_)Φ(_−d_1 (_S∗∗_)) _, γ_<sub>1</sub>

_and <sub>S</sub><sup>∗∗</sup> is the solution of the non-linear equation_

_S∗∗_ _−y_(_T−t_)Φ(_−d_1(_S∗∗_))_._

_K − S∗∗_ \= _p_(_t,T,K |S_ \= _S∗∗_) _−_ 1 _− e_

_γ_<sub>1</sub>

### 3.8.2 Representation of the exercise frontier

If the exercise frontier were known, the valuation of an American option would be considerably simplified. Indeed, the American option essentially pays a cash flow the first time that the UA price hits the exercise frontier (if ever). It turns out that the first hitting time of a Brownian motion to a constant barrier has an explicit probability distribution (see for example Karatzas and Shreve, 1991, and this book chapter on exotic options). Omberg (1987) and Chesney and Lefoll (1996) build on this result to value American options assuming the exponential shape of the exercise frontier for the American put.

Unfortunately the exact shape of the exercise boundary is not known explicitly. The exponential assumption yields to a crude approximation of the American option premium, and Omberg (1987) suggests a numerical optimization to reduce the pricing error. That optimization consists in finding the exponential exercise frontier that is the least distant to the true boundary.

More fundamentally, Kim (1990), Jacka (1991) and Carr et al. (1992) show that, under the BMS assumptions, the difference in put option premiums _<sub>P</sub>_(0_<sub>,T,K</sub>_) _− <sub>p</sub>_(0_<sub>,T,K</sub>_) can be rewritten as

Z _T_ <sub>i</sub>

<sup>h</sup>_rKe<sup>−rt</sup>_Φ(_−d_<sub>2</sub>(_S_(0)_,t,B_(_t_))) _− yS_(0)_e<sup>−yt</sup>_Φ(_−d_<sub>1</sub>(_S_(0)_,t,B_(_t_))) d_t,_

0

_<sup>k</sup>_ <sup>2</sup> _t_ where _<sub>B</sub>_(_<sub>t</sub>_) denotes the exercise frontier and, _<sub>d</sub>_<sub>1</sub>_<sub>,</sub>_<sub>2</sub>(_<sub>x,t,k</sub>_) = _√_ .

_σ t_

Note that it does not matter if we approach the American option pricing problem with the put, since the American call premium can be retrieved from the American option symmetry.

To gain a better insight of the integral representation of the put early exercise premium, Jamshidian (1992) offers the following interpretation. The early exercise premium can be viewed as the compensation that the option buyer should receive to postpone the exercise of the option. When the UA hits the exercise frontier _<sub>B</sub>_(_<sub>t</sub>_) (which occurs with probability Φ(_<sub>−d</sub>_<sub>2</sub>(_<sub>S</sub>_(0)_<sub>,t,B</sub>_(_<sub>t</sub>_)))), the put owner could receive the exercise price (and earn the present value of interests _<sub>rK</sub>_ generated from capital _<sub>K</sub>_), and in counterpart could deliver the UA (and thus give up receiving the dividends paid at the continuous rate _<sub>y</sub>_). The compensation to postpone the early exercise of the put thus corresponds to the cash flow (_<sub>rK − yS</sub>_(_<sub>t</sub>_)) per unit of time between the exercise date and expiration. This cash flow is discounted conditionally on the fact that the UA hits the barrier (the conditioning uses probability Φ(_<sub>−d</sub>_<sub>2</sub>(_<sub>S</sub>_(0)_<sub>,t,B</sub>_(_<sub>t</sub>_))) for a monetary cashflow and probability Φ(_<sub>−d</sub>_<sub>1</sub>(_<sub>S</sub>_(0)_<sub>,t,B</sub>_(_<sub>t</sub>_))) for a cashflow related to the UA), and integrated over all the possible exercise times between 0 and _<sub>T</sub>_.

Suppose there is a time _<sub>t</sub>_ when _<sub>S</sub>_(_<sub>t</sub>_) = _<sub>B</sub>_(_<sub>t</sub>_), then _<sub>P</sub>_(_<sub>t,T</sub> −<sub>t,K</sub> |<sub>S</sub>_ \= _<sub>B</sub>_(_<sub>t</sub>_)) = _<sub>K</sub> −<sub>B</sub>_(_<sub>t</sub>_) and the integral representation of the put early exercise premium can be rewritten as

_K − B_(_t_)

\= _p_(_t,T,K |S_ 

Z _T_

_− K re<sup>−r</sup>_<sup>(</sup>_<sup>s−t</sup>_<sup>)</sup>Φ(_d_<sub>2</sub>(_B_(_t_)_,s − t,B_(_s_)))d_s_

_t_

<sup>Z</sup> _T_

\+ _B_(_t_) _ye<sup>−y</sup>_<sup>(</sup>_<sup>s−t</sup>_<sup>)</sup>Φ(_d_<sub>1</sub>(_B_(_t_)_,s − t,B_(_s_)))d_s_ (3.11)

_t_

which must be numerically solved to get all the points _<sub>B</sub>_(_<sub>t</sub>_), _<sub>t ∈</sub>_ \[0_<sub>,T</sub>_\]. Huang et al. (1996), Ju (1998) and Bunch and Johnson (2000) propose different algorithms towards this end.

As noted by Carr et al. (1992), the non-dividend case (_<sub>y</sub>_ \= 0) can be simplified significantly. Indeed, the put early exercise premium is simply

Z _T_

_v_ \= _rK e<sup>−rt</sup>_Φ(_−d_<sub>2</sub>(_S_(0)_,t,B_(_t_)))d_t._ (3.12)

0

The put delta and gamma can be obtained directly by differentiation

∆_v_ \= _−rK_ Z _T √_ d_t,_

_σS_ <sub>0</sub> 2_πt_

Γ_v_ \= _rK√_ Z _T e−rte−b_22 _√_1 _− b_ d_t,_

_S_<sup>2</sup>_σ_ ~~2~~_π_ <sub>0</sub> _t σt_

with

_b_ \= _−d_<sub>2</sub>(_S,t,B_(_t_))_._

Carr et al. (1992) show that the exercise frontier has the following functional form:

#

_Btm ,_

where _<sub>m</sub>_ is the root of the following equation

#

_r_

erf

r

h

1

2

_β_

(

_τ_

)

2

+

_r_

i

_τ_

_τm_ Φ(_−m_) = q _,_

_β_ (_τ_)2 + 2_r_

with _<sub>τ</sub>_ \= _<sub>T</sub> − <sub>t</sub>_ and

_,_

erf (_<sub>x</sub>_) = 2Φ _<sub>.</sub>_

### 3.8.3 Numerical comparison

To better gauge the quality of the quasi-analytical methods presented above, we proceed to a numerical comparison of their pricing performance. The table below reports the American put premium using the Barone-Adesi and Whaley (1987) approximation (BAW) and the Carr et al. (1992) integral formula (CJM).

Fixed parameters are _<sub>K</sub>_ \= 100, _<sub>r</sub>_ \= 5%, _<sub>y</sub>_ \= 0, and _<sub>σ</sub>_ \= 30%. These put premiums are compared to their “true value”, defined as the value obtained from a time-consuming but sufficiently accurate numerical method – in this case a binomial tree with 10,000 time steps ensuring 3-digit precision (see the next chapter for a presentation).

|     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- |
|     | 1-<br><br>_S_ \= 90 | month options<br><br>_S_ \= 100 | _S_ \= 110 | 6-<br><br>_S_ \= 90 | month options<br><br>_S_ \= 100 | _S_ \= 110 |
| “True” | 10.231 | 3.271 | 0.567 | 12.750 | 7.394 | 3.996 |
| BAW | 10.201 | 3.265 | 0.569 | 12.692 | 7.385 | 4.011 |
| CJM | 10.232 | 3.272 | 0.567 | 12.750 | 7.395 | 3.996 |

## 3.9 Problem set

#### Exercise 3.1

Show that the BMS European call premium is a decreasing, convex function of the strike price. Hint: You may need to use the fact that

_Ke−rT ϕ_(_d_2) = _Se−yT ϕ_(_d_1)_,_

where _<sub>ϕ</sub>_(_<sub>.</sub>_) is the standard normal density.

#### Exercise 3.2

From the BMS European call option formula:

1.  Compute the limit of _<sub>c</sub>_(_<sub>t,T,K</sub>_) when volatility _<sub>σ</sub>_ approaches to zero and when volatility _<sub>σ</sub>_ tends to infinity.
2.  Provide a financial interpretation for these results.

#### Exercise 3.3

Consistent with the BMS framework, the price process _<sub>S</sub>_ is assumed to be driven by the following stochastic differential equation under the EMM

<sup>d</sup>_<sup>S</sup>_(<sup>(</sup>_t_)_<sup>t</sup>_<sup>)</sup> \= _r_d_t_ \+ _σ_ d_Z_(_t_)_. S_

1.  Use Itˆo’s lemma to derive the solution to this stochastic differential equation.
2.  Compute E<sup>Q</sup> \[_<sub>S</sub>_(_<sub>T</sub>_)\] where _<sub>T</sub>_ stands for an arbitrary future date.
3.  Consider the stochastic process _<sub>G</sub>_(_<sub>t</sub>_) defined by _<sub>G</sub>_(_<sub>t</sub>_) = (_<sub>S</sub>_(_<sub>t</sub>_))_<sup>α</sup>_, where _<sub>α</sub>_ is a real constant. Use the result found in question a) to compute E<sup>Q</sup> \[_<sub>G</sub>_(_<sub>T</sub>_)\]
4.  Determine the only two possible values of _<sub>α</sub>_ so that _<sub>G</sub>_ represents the price process of an asset traded on a financial market.
5.  Recover the result in question d) by applying Itˆo’s lemma directly on the process _<sub>G</sub>_.

#### Exercise 3.4

_Siegel’s paradox_. Under the BMS framework, the stochastic differential equation driving the exchange rate _X_, that is, the price of one unit of foreign currency expressed in domestic currency is, under the domestic risk-neutral probability measure Q_d_,

_dX_((_tt_)) = (_rd − rf_) d_t_ \+ _σ_ d_Z_(_t_)_,_

_X_

where _<sub>rd</sub>_ and _<sub>rf</sub>_ stand for the domestic and foreign money market rates, respectively.

1.  Let _<sub>Y</sub>_ denote the price of one unit of domestic currency expressed in foreign currency. In other words, _<sub>Y</sub>_ is the exchange rate for the foreign investor. Using Itˆo’s lemma, determine the risk-neutral dynamics for _<sub>Y</sub>_ .
2.  Why is the result found in question a) a paradox? (c) Consider the following change of probability measure

_d_Q_f_!

_t ._

_d_Q_d_

Using Girsanov theorem, write the dynamics of _<sub>Y</sub>_ under Q_f_. Explain the solution to the paradox.

**Exercise 3.5**

Derive the valuation formula for the perpetual call under the BMS framework assuming _<sub>y ></sub>_ 0.

#### Exercise 3.6

Consider two traded assets with price dynamics under Q given by

_dA_((_<sub>t</sub>t_)) = (_r − yA_) d_t_ \+ _σA_ d_Z_(_t_)_A, <sub>A</sub>_

_<sup>dB</sup>_(<sup>(</sup>_t<sup>t</sup>_)<sup>)</sup> \= (_r − y<sub>B</sub>_) d_t_ \+ _σ<sub>B</sub>_ d_Z_(_t_)_<sup>B</sup>, B_

where _<sub>Z</sub>_(_<sub>t</sub>_)_<sup>A</sup>_ and _<sub>Z</sub>_(_<sub>t</sub>_)_<sup>B</sup>_ are two correlated Brownian motions such that d_<sub>Z</sub>_(_<sub>t</sub>_)_<sup>A</sup>_ d_<sub>Z</sub>_(_<sub>t</sub>_)_<sup>B</sup>_ \= _<sub>ρ</sub>_d_<sub>t</sub>_. The goal is to evaluate the European-style call option _<sub>g</sub>_ offering the terminal payoff at time _<sub>T</sub>_

_g_(_T_) = max0_, BA_((_TT_)) _− K._

1.  Using the solutions to the Geometric Brownian Motions (GBM) _<sub>A</sub>_(_<sub>t</sub>_) and _<sub>B</sub>_(_<sub>t</sub>_), show that the process _A_(_<sub>t</sub>_)_<sub>/B</sub>_(_<sub>t</sub>_) is also a GBM and characterize its volatility _<sub>σ</sub>_ and dividend yield _<sub>y</sub>_.
2.  Making the analogy with the BMS call option formula, derive the value of _<sub>g</sub>_.
3.  Give a sufficient condition for the American call written on _<sub>A</sub>_(_<sub>t</sub>_)_<sub>/B</sub>_(_<sub>t</sub>_)to have the same value as _<sub>g</sub>_.

#### Exercise 3.7

The _break forward_ contract (with value denoted by _<sub>BF</sub>_(_<sub>t</sub>_)) is a slight alteration to the forward contract as it offers the terminal payoff

_BF_(_T_) = max\[_S_(_T_)_,f_ (0_,T_)\] _− K,_

where _<sub>f</sub>_(0_<sub>,T</sub>_) is the time-0 forward price of the UA _<sub>S</sub>_ for a time-_<sub>T</sub>_ delivery and _<sub>K</sub>_ is a constant.

1.  Rewrite _<sub>BF</sub>_(_<sub>T</sub>_) by highlighting the terminal payoff of a European call written on _<sub>S</sub>_ and propose a parity relation at time 0 between the break forward contract and that European call in the AoA.
2.  In practice, the constant _<sub>K</sub>_ is set in such a way that the initial cost of the break forward contract is nil. Determine the value of _<sub>K</sub>_ in the BMS framework using the cash & carry relation and assuming the UA pays no dividend until _<sub>T</sub>_.

#### Exercise 3.8

Value-at-Risk (_<sub>V aR</sub>_) and expected shortfall (_<sub>ES</sub>_) are two metrics commonly used in risk management. The return _<sub>V aR</sub>_ of a portfolio can be defined as the return that the portfolio will achieve at time _<sub>T</sub>_ in the (1 _<sub>− α</sub>_) % of the worst scenarios. Formally, let _<sub>R</sub>_(_<sub>T</sub>_) denote the continuously compounded return on the portfolio at horizon _<sub>T</sub>_, then

1 _− α_ \= P(_R_(_T_) _< V aR<sub>α,T</sub>_ )_._

In addition, _<sub>ES</sub>_ represents the expected loss on a portfolio conditional on the return on that portfolio being below the return _<sub>V aR</sub>_. Formally,

_ESα,T_ \=Z 1 _V aRu,T du,_

_α_

1.  Propose an explicit formula for the _<sub>V aR</sub>_ in the BMS fra_<sub>√</sub>_mework where _<sub>R</sub>_(_<sub>T</sub>_) is assumed to be normally distributed with mean _<sub>µT</sub>_ and standard deviation _<sub>σ T</sub>_.
2.  Compute the one-day, 99% return _<sub>V aR</sub>_ for a portfolio with 10% annual expected return and 30% annual return volatility.
3.  Propose an explicit formula for the _<sub>ES</sub>_ in the BMS framework. Compute the one-day, 99% _<sub>ES</sub>_ for the same portfolio.

#### Exercise 3.9

Consider the following two perpetual options. Option A offers $1 the first time the price of an UA hits the upper level _<sub>H</sub>_. Option B offers $1 the first time the price of that same UA hits the lower level _<sub>L</sub>_. Let _<sub>S</sub>_ denote the price process of the UA. Currently we have _<sub>L < S < K</sub>_. The UA does not pay any dividend.

1.  Since A and B are perpetual options, write down the ODE that their premiums satisfy in the BMS framework.
2.  Verify that the form of the solution for the two premiums is

_aS_ \+ _bS−σ_2_r_2 _,_

where _<sub>r</sub>_ is the risk-free rate, _<sub>σ</sub>_ is the UA price volatility, and _<sub>a</sub>_ and _<sub>b</sub>_ are two constants to be determined by boundary conditions.

1.  What is option A worth when _<sub>S</sub>_ is equal to zero? What is option B worth when _<sub>S</sub>_ goes to infinity? Refine the expression for the two option premiums.
2.  Applying the boundary condition _<sub>A</sub>_(_<sub>H</sub>_) = _<sub>B</sub>_ (_<sub>L</sub>_) = 1, give a final expression for the two premiums.

#### Exercise 3.10

The payoff of a _calendar spread_ is the difference between two prices of the same UA observed at two different dates. For instance, the calendar spread on the forward price offers at time _<sub>b</sub>_ the amount _<sub>f</sub>_ (_<sub>b,T</sub>_)_<sub>−f</sub>_ (_<sub>a,T</sub>_) where _<sub>a</sub>_ and _<sub>b</sub>_ are the two observation dates and _<sub>T</sub>_ is the delivery date (_<sub>a < b < T</sub>_).

1.  Recall the expression of the forward price _<sub>f</sub>_ (_<sub>t,T</sub>_) in the BMS framework.
2.  Use that expression to infer the value of the calendar spread at time 0.
3.  What is the value of the calendar spread at time _<sub>u</sub>_ with _<sub>a < u < b</sub>_?

#### Exercise 3.11

Consider the European option on a calendar spread (also known as the _forward start_ option) with terminal payoff

_g<sub>T</sub>_<sub>2</sub> \= max(0_,S<sub>T</sub>_<sub>2</sub> _− S<sub>T</sub>_<sub>1</sub>)_,_

where _<sub>S</sub>_(_<sub>t</sub>_) denotes the spot price process of the UA, and _<sub>T</sub>_<sub>1</sub> and _<sub>T</sub>_<sub>2</sub> are two observation dates (_<sub>T</sub>_<sub>1</sub> _<sub>< T</sub>_<sub>2</sub>).

1.  Evaluate the forward start option at time _<sub>T</sub>_<sub>1</sub> (note that, by design, this option is ATM at time _<sub>T</sub>_<sub>1</sub>).
2.  Using the fact that, at time _<sub>T</sub>_<sub>1</sub>, the value of the forward start option is a deterministic quantity of the UA, evaluate the contract at time 0.

#### Exercise 3.12

Consider the European-type structured product offering the following terminal payoff

<sup></sup><sub></sub> 0 if _S_(_T_) _≤ K, g_(_T_) = _M_ if _K < S_(_T_) _≤ L,_

<sup></sup><sub></sub> _αS_(_T_) if _L < S_(_T_)_,_

where _<sub>S</sub>_(_<sub>t</sub>_) denotes the spot price process of the UA, and _<sub>α</sub>_, _<sub>K</sub>_, _<sub>L</sub>_ and _<sub>M</sub>_ are constants.

1.  Show that the payoff can be synthetically replicated with a combination of digital options.
2.  Using the replication strategy from question a), propose a valuation formula for _<sub>g</sub>_ in the BMS framework.

## 3.10 Solutions

#### Solution 3.1

The first order partial derivative of the call premium with respect to the strike price is

_∂c ._

The second order derivative is

_∂_<sup>2</sup>_c_

(

_t,T,K_

)

_∂K_

2

\=

exp(

_−_

_r_

(

_T_

_−_

_t_

))

_Kσ_

_T_

_t_

_ϕ_

(

_d_

2

)

_\>_

0

_√ . −_

The call premium is therefore a decreasing, convex function of the strike price.

#### Solution 3.2

1.  For _<sub>c</sub>_(0_<sub>,T,K</sub>_), as _<sub>σ</sub>_ goes to zero

|     |     |
| --- | --- |
| lim <sup>h</sup> _−yT_ Φ( ) _− −rT_ Φ( )<sup>i</sup> \= _−yT_ 1 _− −rT_ 1 |     |
| _Se σ→_0<sup>+</sup><br><br>Similarly, | _d_1 _Ke d_2 _<sup>Se</sup> Se−yT>Ke−<sup>rT Ke</sup> Se−yT>Ke−rT_ \= _−yT − Ke−rT_ \+ _._<br><br>_Se_<br><br>lim h _−yT_ Φ( 1) _− Ke−rT_ Φ(_d_2)i = _Se−yT ._<br><br>_Se d_ |

_σ→_+_∞_

1.  When the UA price is no more volatile, the call option loses all of its speculative value and its premium is reduced to the intrinsic value. By contrast, when the UA price gets extremely volatile, the call premium is mostly comprised of the speculative value and becomes a linear function of the UA price.

#### Solution 3.3

1.  Applying Itˆo’s lemma on ln_<sub>S</sub>_ one gets

" _σ_2 ! # _S_(_t_) = _S_ exp _r −_ 2 _t_ \+ _σZ_(_t_) _._

1.  Taking the expectation of _<sub>S</sub>_(_<sub>T</sub>_)

!#

 E<sup>Q</sup> \[_S_(_T_)\] = _Se<sup>rT</sup>_ E = _Se<sup>rT</sup> ,_

since the expression inside the expectation is a martingale.

1.  Using the solution obtained in question a)

_G_(_t_) = _Sα_ exp"_α_ _r − σ_22 !_t_ \+ _ασZ_(_t_)#_._

Hence

E<sup>Q</sup> \[_G_(_T_)\] = _S<sup>α</sup>_ exp _αrT_

\= _Sα_ exp _αrT_ _T_

 = _G_exp _αrT._

1.  For _<sub>G</sub>_ to represent the price process of a traded asset, it must be a martingale under Q once discounted at the risk-free rate. Thus, it must be that

_αr_ \+ _α_2_σ_2 _− ασ_2 2 = _r,_

that is,

_ασ_2 !

(_α −_ 1) _r_ \+ 2 = 0_._

The only two possible values for _<sub>α</sub>_ are therefore 1 and _<sub>−</sub>_2_<sub>r/σ</sub>_<sup>2</sup>. (e) Using Itˆo’s lemma on _<sub>G</sub>_

_dG_ \= _αS<sup>α−</sup>_<sup>1</sup> d_S_ \+ _α_(_α −_ 1)_S<sup>α−</sup>_<sup>2</sup> (d_S_)<sup>2</sup> _._

Hence

 _dG_ d_S_ +_α_(_α −_ 1) d_S_<sup>2</sup>

\= _α_

_G SS_

\= _αr_ \+ _α_(_α −_ 1)_σ_2 d_t_ \+ _ασ_ d_Z_(_t_)_._

For exp(_<sub>−rt</sub>_)_<sub>G</sub>_(_<sub>t</sub>_) to be a martingale, it must be that

_αr_ \+ _α_(_α −_ 1)_σ_<sup>2</sup> \= _r,_

which leads to the same conclusion as in question d).

#### Solution 3.4

1.  Applying Itˆo’s lemma on _<sub>Y</sub>_ \= 1_<sub>/X</sub>_

_dY_ \= _−_ 1<sub>2</sub> _dX_ \+ 21 _<sub>X</sub>_2<sub>3</sub> (_dX_)<sup>2</sup> _<sub>X</sub>_

\= 1 (_re − rd_) d_t −_ 1 _σ_ d_Z_(_t_) + 1 _σ_2 d_t,_

_X X X_

or, alternatively,

_<sup>dY</sup>_ <sup>2</sup> d_t − σ_ d_Z_(_t_)_._

\= _r<sub>e</sub> − r<sub>d</sub>_ \+ _σ_

_Y_

1.  The result in question a) seems to be a paradox as one would maybe have expected to find the opposite dynamics for _<sub>Y</sub>_ . That is, if the exchange rate appreciates at rate _<sub>rd</sub> − <sub>re</sub>_ for the domestic investor, it should depreciate at the same rate for the foreign investor.
2.  From Girsanov theorem, the process _<sub>Z</sub>_(_<sub>t</sub>_)_<sup>f</sup>_ := _<sub>Z</sub>_(_<sub>t</sub>_) _<sub>− σt</sub>_ is a Q_f−_Brownian motion. The dynamics

|     |     |     |
| --- | --- | --- |
| of _<sub>Y</sub>_ under Q_f_ are therefore |     |     |
| _dY_<br><br>_Y_ | \=  | _r − r_ \+ _σ_ _e d_ 2 d_t − σ_ d_Z_(_t_)_f_ \+ _σ_ d_t_ |
|     | \=  | (_r<sub>e</sub> − r<sub>d</sub>_) d_t − σ_ d_Z_(_t_)_<sup>f</sup>._ |

The solution to the paradox is that the dynamics of _<sub>Y</sub>_ is indeed the opposite of that of _<sub>X</sub>_ but under the _foreign_ risk-neutral probability measure Q_f_.

#### Solution 3.5

The perpetual call and put satisfy the same ODE. Therefore

_C<sub>∞</sub>_(_S_) _≡ C_(_t,∞,K |S_(_t_) = _S_) = _a_<sub>1</sub>_S<sup>αp</sup>_ \+ _a_<sub>2</sub>_S<sup>αc</sup>._

The boundary conditions associated with the perpetual call are

|     |     |     |
| --- | --- | --- |
| lim_C<sub>∞</sub>_(_S_)<br><br>_S→_0 | \=  | 0_,_ |
| _C<sub>∞</sub>_(_S<sup>∗</sup>_) | \=  | _S<sup>∗</sup> − K,_ |

which yields _a_<sub>1</sub> \= 0, _a_<sub>2</sub>_S<sup>∗αc</sup>_ \= _S<sup>∗</sup> − K_, and

_C<sub>∞</sub>_(_S_) = (_S∗ − K_) _S∗ αc ._

_S_

First order condition yields _<sub>S</sub>__<sub>K</sub>_ and finally

_C∞_(_S_) = _α<sub>c</sub>K−_ 1 _αcα−c_ 1 _KS αc ._

Note: the condition _<sub>y ></sub>_ 0 entails that _<sub>αc ></sub>_ 1.

#### Solution 3.6

1.  Given the expressions for _<sub>A</sub>_(_<sub>t</sub>_) and _<sub>B</sub>_(_<sub>t</sub>_)

_A_(_t_) = _A_ exp _−yA_ \+ _yB − σA_2

_B_(_t_) _B_ " 2 + _σ_2_B_2 !_t_ \+ _σAZ_(_t_)_A − σBZ_(_t_)_B_#_._

The process _σ<sub>A</sub>Z_(_t_)_<sup>A</sup> − σ<sub>B</sub>Z_(_t_)_<sup>B</sup>_ has the same law as _σW_(_t_) with _σ_ \= <sup>q</sup>_σ<sub>A</sub>_<sup>2</sup> \+ _σ<sub>B</sub>_<sup>2</sup> _−_ 2_σ<sub>A</sub>σ<sub>B</sub>ρ_ and

_W_(_<sub>t</sub>_) a Brownian motion. Thus

_A_(_t_) = _A_ exp" _−yA_ \+ _yB_ \+ _σ_2 _− σ_2 ! #

_B_(_t_) _B B σAσBρ −_ 2 _t_ \+ _σW_(_t_) _._

The process _<sub>A</sub>_(_<sub>t</sub>_)_<sub>/B</sub>_(_<sub>t</sub>_) is therefore a GBM with volatility _<sub>σ</sub>_ and dividend yield _<sub>y</sub>_ \= _<sub>r</sub>_ \+ _<sub>yA</sub> − <sub>yB</sub> − σB_2 + _σAσBρ_.

1.  The valuation formula for _<sub>g</sub>_ is

_g_ \= _Ae−yT_ Φ(_z_1) _− Ke−rT_ Φ(_z_2)_, B_

with

_z_1 = ln _BKA_ \+ _r√−y_\+ _T , z_2 = _z_1 _− σ√T._

_σ T_

1.  The American call has the same value as _<sub>g</sub>_ if the UA pays no positive dividend, that is, if

_r_ \+ _y<sub>A</sub> − y<sub>B</sub> − σ<sub>B</sub>_<sup>2</sup> \+ _σ<sub>A</sub>σ<sub>B</sub>ρ <_ 0_._

#### Solution 3.7

(a) Rearranging the expression for _<sub>BF</sub>_(_<sub>T</sub>_)

_BF_(_T_) = max\[_S_(_T_) _− f_ (0_,T_)_,_0\] + _f_ (0_,T_) _− K,_

hence the parity relation at time 0

_BF_(0) _− c_(0_,T,f_(0_,T_)) = \[_f_ (0_,T_) _− K_\]_e<sup>−rT</sup> ._ (b) In the absence of dividends, the forward price is _<sub>f</sub>_ (0_<sub>,T</sub>_) = _<sub>S</sub>_(0)_<sub>e</sub><sup>rT</sup>_ and, for a call struck at _<sub>f</sub>_ (0_<sub>,T</sub>_), we have that _<sub>d</sub>_<sub>1</sub>_<sub>,</sub>_<sub>2</sub> _<sub>T</sub>_. Hence, the condition _<sub>BF</sub>_(0) = 0 yields

\=

h

log

_S_

(0)

_f_

(0

_,T_

)

+

_r_

_±_

1

2

_σ_

2

i

_/_

(

_σ_

_√_

_T_

)=

_±_

1

2

_σ_

_√_

0=

_c_

(0

_,T,f_

(0

_,T_

))+\[

_f_

(0

_,T_

)

_−_

_K_

\]

_e_

_−_

_rT_

\=

_S_

(0)Φ

1

2

_σ_

_√_

_T_

_−_

\[

_S_

(0)

_e_

_rT_

\]

_e_

_−_

_rT_

Φ

_−_

1

2

_σ_

_√_

_T_

+

h

_S_

(0)

_e_

_rT_

_−_

_K_

i

_e_

_−_

_rT_

\=

_S_

(0)

Φ

1

2

_σ_

_√_

_T_

_−_

1

_−_

Φ

1

2

_σ_

_√_

_T_

+

_S_

(0)

_−_

_Ke_

_−_

_rT_

\=2

_S_

(0)Φ

1

2

_σ_

_√_

_T_

_−_

_Ke_

_−_

_rT_

which implies that

_K_ _._

#### Solution 3.8

1.  Since _R_(_T_) _∼ N µT,σ√T_

P(_R_(_T_) _< V aRα,T_ ) = Φ_V aRα,T√ − µT , σ T_

and therefore _<sub>√</sub>_

_V aR<sub>α,T</sub>_ \= _µT_ \+ _σ T_Φ_<sup>−</sup>_<sup>1</sup> (1 _− α_)_._

1.  The numerical application yields

_._

1.  From the expression of _<sub>V aRα,T</sub>_

\= 1 1 _√_

_ESα,T_ 1 _− α_ Z_α µT_ \+ _σ T_Φ_−_1 (1 _− u_)_du_

\= _µT_ _du._

To compute the integral, we proceed to the following change of variable: _<sub>u</sub>_ \= Φ(_<sub>y</sub>_), _<sub>du</sub>_ \= _<sub>ϕ</sub>_(_<sub>y</sub>_)_<sub>dy</sub>_, which yields

<sub>Z</sub> 1 Z Φ_<sup>−</sup>_<sup>1</sup>(1)

_du_ \= _dy_

<sup>Z</sup> _∞_ \= _− yϕ_(_y_)_dy_

_−_

_._

Hence

 _ES<sub>α,T</sub>._

The numerical application yields

_ES__._

#### Solution 3.9

1.  Let _<sub>gi</sub>_, _<sub>i</sub>_ \= _<sub>{A,B}</sub>_, denote the premium of either option A or option B. In the AoA, _<sub>gi</sub>_ is solution to

 _rg<sub>i</sub>._

1.  Let _<sub>gi</sub>_ \= _<sub>aS</sub>_ \+ _<sub>bS</sub><sup>−</sup><sub>σ</sub>_<sup>2</sup>_<sup>r</sup>_<sup>2</sup> . Then, the left-hand side of the ODE is

_a −_ 2_r_2 _bS−σ_2_r_2 _−_1_rS_ \+ 21 _σ_2_r_2 _σ_2_r_2 + 1_bS−σ_2_r_2 _−_2_σ_2_S_2 _σ_

\= _arS −_ 2_σr_22 _bS−σ_2_r_2 + 2_σr_22 + _r_!_bS−σ_2_r_2

\= _raS_ \+ _bS−σ_2_r_2 _,_

which is equal to the right-hand side of the ODE.

1.  By definition, _<sub>gA</sub>_ (_<sub>S</sub>_ \= 0) = 0, hence the constant _<sub>b</sub>_ must be nil. By definition, _<sub>gB</sub>_ (_<sub>S</sub> → ∞_) = 0, hence the constant _<sub>a</sub>_ must be nil. Thus

_gA_ \= _aS, gB_ \= _bS−σ_2_r_2 _._

1.  Using _<sub>gA</sub>_ (_<sub>S</sub>_ \= _<sub>H</sub>_) = 1 and _<sub>gB</sub>_ (_<sub>S</sub>_ \= _<sub>L</sub>_) = 1, we finally obtain

_gA H , gB_ \= _LS −σ_2_r_2 _._ \= _S_

#### Solution 3.10

1.  In the BMS framework, the forward price follows a GBM with no drift, i.e.

_σ_2 !

_f_ (_t,T_) = _f_ (0_,T_)exp _σW_(_t_) _−_ 2 _t ._

1.  The value of the calendar spread a time 0 is given by

_e<sup>−rT</sup>_ E<sup>Q</sup> \[_f_ (_b,T_) _− f_ (_a,T_)\] = 0_._

1.  At time _<sub>u</sub>_, the forward price _<sub>f</sub>_ (_<sub>a,T</sub>_) is a known quantity. The calendar spread is therefore worth

_e<sup>−r</sup>_<sup>(</sup>_<sup>T−u</sup>_<sup>)</sup> E<sup>Q</sup><sub>u</sub> \[_f_ (_b,T_) _− f_ (_a,T_)\] = _e<sup>−r</sup>_<sup>(</sup>_<sup>T−u</sup>_<sup>)</sup> \[_f_ (_u,T_) _− f_ (_a,T_)\]_._

#### Solution 3.11

1.  At time _<sub>T</sub>_<sub>1</sub>, we apply the BMS valuation formula for the ATM call, which yields

_c_(_T_1_,T_2_,S_(_T_1)) = _S_ (_T_1)h_e−y_(_T_2_−T_1)Φ(_d_1) _− e−r_(_T_2_−T_1)Φ(_d_2)i_,_

with

_d_1 = _r − y_ \+ _σ_2p_T_2 _− T_1_, σ d_2 = _r − y − σ_2p_T_2 _− T_1_. σ_

1.  This value at time _<sub>T</sub>_<sub>1</sub> can also be written as follows

_c_(_T_<sub>1</sub>_,T_<sub>2</sub>_,S_(_T_<sub>1</sub>)) = _S_(_T_<sub>1</sub>)_φ_(_T_<sub>2</sub> _− T_<sub>1</sub>)_,_

where _<sub>φ</sub>_(_<sub>T</sub>_<sub>2</sub> _− <sub>T</sub>_<sub>1</sub>) is a deterministic function of _<sub>r</sub>_, _<sub>y</sub>_, _<sub>σ</sub>_ and _<sub>T</sub>_<sub>2</sub> _− <sub>T</sub>_<sub>1</sub>. Thus, in the AOA, the initial value of the forward start call is

_cfwd_ \= _Se−yT_1_φ_(_T_2 _− T_1)_._

#### Solution 3.12

1.  The payoff can be written as follows

_g_(_T_) = _M_1_S_(_T_)_≤L − M_1_S_(_T_)_<K_ \+ _αS_(_T_)1_S_(_T_)_\>L._

Hence the structured product can be replicated by selling a cash-or-nothing put with strike price _<sub>K</sub>_, buying a cash-or-nothing put with strike price _<sub>L</sub>_ and buying an asset-or-nothing call with strike price _L_.

1.  In the BMS framework, these three digital options are worth

_g_ \= _Me<sup>−rT</sup>_ Φ(_x_<sub>1</sub>) _− Me<sup>−rT</sup>_ Φ(_x_<sub>2</sub>) + _αSe<sup>−yT</sup>_ Φ(_x_<sub>3</sub>)_,_

with

ln _S_ +_r−y−σ_2 _T x_<sub>1</sub> \= _− √ , L_ 2 _σ T_

ln _<sup>S</sup>_ +_r−y−<sup>σ</sup>_<sup>2</sup> _T x_<sub>2</sub> \= _− √ , K_ 2 _σ T_

ln _<sup>S</sup>_ +_r−y_+_<sup>σ</sup>_<sup>2</sup> _T x_<sub>3</sub> \= _√ . L_ 2

_σ T_

**Chapter 4**

# Discrete-Time Approach

An alternative approach to the valuation of derivatives consists in building a discrete time tree that specifies a limited set of states of nature across time. In this chapter, we start by reviewing the binomial model developed by Cox et al. (1979) and Rendleman and Bartter (1979) and the way it converges to the continuous time, BMS model. We also present the alternative design of the binomial tree proposed by Jarrow and Rudd (1983). Pricing accuracy can be improved by resorting to trinomial trees. There are several ways to construct them and we discuss some of the possibilities.

In the second part of this chapter, we examine the fundamental issue of replication. In the BMS model, it is possible to perfectly replicate the payoff of a European option by means of a self-financing portfolio strategy. In the AoA, the value of the derivative must therefore be equal to the initial cost of this portfolio. The equivalence between derivatives valuation and replication is a neat feature of the BMS model. However, it requires the continuous rebalancing of the replicating portfolio. Thus, perfect replication is no longer feasible in discrete time. We investigate how the imperfection of replication can be reduced by implementing a hedging strategy. For agents selling options, relying on such a hedging strategy is crucial to avoid severe losses.

## 4.1 Standard binomial trees

We assume a binomial distribution of the UA. The possible paths of the UA are represented using a tree. The time is discrete. Let _<sub>T</sub>_ be the expiration date of the derivative, the time interval \[0;_<sub>T</sub>_\] is subdivided into subintervals of length <sub>∆</sub>_<sub>t</sub>_, with _<sub>tn</sub>_ \= _<sub>n</sub>_<sub>∆</sub>_<sub>t</sub>_ for _<sub>n</sub>_ \= 0_<sub>,...,N</sub>_. At each point in time, given its previous value, the UA can take two values depending on whether it moves up or down. These values are obtained by scaling the previous value of the UA by _<sub>un</sub>_ for an upward move and _<sub>dn</sub>_ for a downward move. Strictly speaking, there is 2_<sup>n</sup>_ possible values for the UA at _<sub>tn</sub>_ without any constraints on _<sub>u</sub>_s and _<sub>d</sub>_s. However, to simplify the analysis, we assume that _<sub>u</sub>_ and _<sub>d</sub>_ are constants (i.e., do not depend on _<sub>n</sub>_), such that the tree is recombining. The number of possible values for the UA at time _<sub>tn</sub>_ is thus reduced to _<sub>n</sub>_ \+ 1. Moreover, we follow Cox et al. (1979) and set _<sub>u</sub>_ \= 1_<sub>/d</sub>_. Figure 4.1 shows the dynamics of UA implied by this method.

93

_t_

0

_t_

1

_t_

2

_t_

3

_S_

_Sd_

_Su_

_Sd_

2

_S_

_Su_

2

_Sd_

3

_Sd_

_Su_

_Su_

3

time

Figure 4.1: Dynamics of the UA in a 3-step binomial tree.

### 4.1.1 CRR tree

Intuitively, the parameters _<sub>u</sub>_ and _<sub>d</sub>_ account for_<sub>√</sub>_the volatility _<sub>σ</sub>_ of the UA. Over the time interval of length ∆_<sub>t</sub>_, the UA’s volatility in a BMS economy is _<sub>σ</sub>_ <sub>∆</sub>_<sub>t</sub>_. Denote by _<sub>p</sub>_ the physical probability of the UA making an upward move.

Equating the UA’s returns’ expectation under BMS to the one implied by the tree, we obtain

exp_{_(_µ − y_)∆_t}_ \= _pu_ \+ (1 _− p_)_d,_

which yields

_p_ \= exp_{_(_µ − y_)∆_t} − d<sub>.</sub>_

_u − d_

Now equalizing the variance of the UA’s returns under BMS to the one implied by the tree yields

_σ_<sup>2</sup>∆_t_ \= _pu_<sup>2</sup> \+ (1 _− p_)_d_<sup>2</sup> _−_ \[_pu_ \+ (1 _− p_)_d_\]<sup>2</sup> _._

Replacing _<sub>p</sub>_ by its value, it follows that

_<sub>σ</sub>_2<sub>∆</sub>_<sub>t</sub>_ \= exp_{_(_µ − y_)∆_t} − d<sub>u</sub>_2 + _u −_ exp_{_(_µ − y_)∆_t}<sub>d</sub>_2

_u − d u − d_

exp_{_(_µ − y_)∆_t} − d_ \+ _u −_ exp_{_(_µ − y_)∆_t}d_<sup>2</sup> _._

_− u_

_u − d u − d_

After making some simplifications, we obtain

_σ_<sup>2</sup>∆_t_ \= exp_{_(_µ − y_)∆_t}_(_u_ \+ _d_) _− ud −_ exp_{_2(_µ − y_)∆_t},_

or, equivalently,

_σ_<sup>2</sup>∆_t_ \= exp_{_(_µ − y_)∆_t}_(_u_ \+ _d_) _−_ 1 _−_ exp_{_2(_µ − y_)∆_t}._

One possible solution suggested by Cox et al. (1979) consists in choosing

n _√_ <sub>o</sub>

_u_ \= exp _σ_ ∆_t ,_

<sup>n</sup> _√_ <sup>o</sup> _d_ \= exp _−σ_ ∆_t ._

Indeed, in this case, the previous equation becomes

<sup>n</sup> _√_ <sup>o n</sup> _√_ <sup>o</sup> _σ_<sup>2</sup>∆_t_ \= exp (_µ − y_)∆_t_ \+ _σ_ ∆_t_ \+ exp (_µ − y_)∆_t − σ_ ∆_t −_ 1 _−_ exp_{_2(_µ − y_)∆_t}._

A second order Taylor expansion gives (recall that exp(_<sub>x</sub>_) for _<sub>x</sub>_ close to zero)

 _σ_<sup>2</sup>∆_t ≃ ._

When <sub>∆</sub>_<sub>t</sub>_<sup>2</sup> is negligible, we see that this equality is indeed satisfied.

We will refer to this tree parametrization as the Cox, Ross and Rubinstein tree or simply the CRR tree.

### 4.1.2 Backward induction and the martingale property

The terminal value of a derivative is specified by the terms of the derivative agreement. It is thus possible to draw a second tree that represents the value of the derivative starting from the terminal nodes (sometimes referred to as leaves). The next step is to move backward to the initial point to obtain the value of the derivative at the initial time. This process is known as _backward_ induction.

Generally speaking, consider an UA whose _convenience yield_ is denoted by _<sub>y</sub>_. This rate _<sub>y</sub>_ equates the continuous dividend rate (for an index), the storage cost (which is negative for the gold), the usage value (for oil) or the interest rate on the foreign exchange market (for the foreign exchange). Assuming the value of the derivative to be known at time _<sub>t</sub>_ \+ <sub>∆</sub>_<sub>t</sub>_, how can we get its value at time _<sub>t</sub>_?

Consider the portfolio obtained by shorting the derivative (which we denote by _<sub>g</sub>_) and buying _<sub>h</sub>_ units of the UA. Let _<sub>r</sub>_ be the risk-free rate. Let us now write the value of this portfolio at the times _<sub>t</sub>_ and _<sub>t</sub>_+<sub>∆</sub>_<sub>t</sub>_:

|     |     |     |     |
| --- | --- | --- | --- |
|     | Date _<sub>t</sub>_ | Date _t_ \+ ∆_t_ | Date _t_ \+ ∆_t_ |
|     |     | Down state | Up state |
| Sell the derivative | _−g_ | _−g<sub>d</sub>_ | _−g<sub>u</sub>_ |
| Buy the UA | _hS_ | _h_exp(_y_∆_t_)_Sd_ | _h_exp(_y_∆_t_)_Su_ |
| Net position | _−g_ \+ _hS_ | _h_exp(_y_∆_t_)_Sd − g<sub>d</sub>_ | _h_exp(_y_∆_t_)_Su − g<sub>u</sub>_ |

The number _<sub>h</sub>_ of units of the UA to buy is chosen such that the portfolio is risk-less (its time _<sub>t</sub>_ \+ <sub>∆</sub>_<sub>t</sub>_ value should remain the same whatever the future realized state). Hence, we choose _<sub>h</sub>_ such that

_h_exp(_y_∆_t_)_Sd − g<sub>d</sub>_ \= _h_exp(_y_∆_t_)_Su − g<sub>u</sub>,_

that is

\= exp(_yg_∆_ut_)_−Sg_(_du − d_)_. h_

Under the AoA condition, a risk-less portfolio must earn the risk-free rate. This yields

(_−g_ \+ _hS_)exp(_r_∆_t_) = _h_exp(_y_∆_t_)_Su − g<sub>u</sub>._

Replacing _<sub>h</sub>_ by its value, we obtain

_<sub>g</sub>_ \= exp(_<sub>−r</sub>_<sub>∆</sub>_<sub>t</sub>_)_<sub>g</sub>d <sub>·</sub> u −_ exp_{_(_r − y_)∆_t}_ \+ _<sub>g</sub>u <sub>·</sub>_ exp_{_(_r − y_)∆_t} − d<sub>.</sub>_

_u − d u − d_

Setting

_<sub>q</sub>_ \= exp_{_(_r − y_)∆_t} − d<sub>,</sub>_

_u − d_

we get

1 _<sub>− q</sub>_ \= _u −_ exp_{_(_r − y_)∆_t}<sub>,</sub>_

_u − d_

and

_g_ \= exp(_−r_∆_t_)(_g<sub>d</sub>_ (1 _− q_) + _g<sub>u</sub>q_)_._

The time _<sub>t</sub>_ value of the derivative is the discounted expectation of its time _<sub>t</sub>_ \+ <sub>∆</sub>_<sub>t</sub>_ value, assuming that we interpret _<sub>q</sub>_ and 1_<sub>−q</sub>_ as probabilities (they are both in \[0_<sub>,</sub>_1\] and sum to 1). It is worth noting that whereas the expectation is discounted at the risk-free rate, we never assumed risk-neutrality. On the contrary, we assumed that whoever shorted the derivative was risk averse enough that they would turn around and fully hedge their exposure to the UA.

This result highlights the martingale property of the discounted price of the UA under a probability measure that is different from the historical measure, namely the EMM measure. We thus retrieve in discrete time the same valuation principle that we highlighted in continuous time. In the CRR tree, the risk-neutral pricing rule entails that

- The _<sub>q</sub>_ probability formula is identical to that of the physical probability _<sub>p</sub>_ up to the difference that the physical drift _<sub>µ − y</sub>_ of the UA is replaced by the risk-neutral drift _<sub>r − y</sub>_.
- As <sub>∆</sub>_<sub>t →</sub>_ 0, a second order Taylor expansion shows that

exp_{_(_r − y_)∆_t} −_ exp<sup>n</sup>_−σ<sup>√</sup>_∆_t_<sup>o</sup>

_q_ \= n _√_ o n _√_

exp _σ_ ∆_t −_ exp _−σ_ ∆_t_<sup>o</sup>

_≃_ (_r − y_)∆_t_ \+ ((_r−y_<sub>2</sub>)_<sub>√</sub>_∆_t_)<sup>2</sup> \+ _σ√_∆_t − σ_<sup>2</sup><sub>2</sub>∆_t <sub>,</sub>_

2_σ_ ∆_t_

which yields

_t q__._

Hence

lim _<sub>q</sub>_ \=_<sub>.</sub>_

∆_t→_0

**Example 4.1** _Assume that the volatility of the UA is <sub>σ</sub>_ \= 20%_. The risk-free rate is <sub>r</sub>_ \= 6%_. Our goal is to build a binomial tree with a step of one week that is_ <sub>∆</sub>_<sub>t</sub>_ \= _. The parameters <sub>u</sub>, <sub>d</sub> and <sub>q</sub> are given by_

 r!

_u_ \= exp 0_<sub>.</sub>_2= 1_<sub>.</sub>_0281_<sub>,</sub>_

 r!

_d_ \= exp _−_0_<sub>.</sub>_2= 0_<sub>.</sub>_9726_<sub>,</sub>_

exph0_._06521 i _−_ exp_−_0_._2q521 _q_ \= q q = 0_._5139_._ exp 0_._2 <sub>52</sub><sup>1</sup> _−_ exp _−_0_._2 <sub>52</sub><sup>1</sup>

### 4.1.3 Pricing algorithm

Once the price of the UA is expanded throughout the tree, the martingale property in a risk-neutral world allows us to obtain the derivative price using backward induction. For a European call, we can simply start by writing the terminal conditions, as shown in Figure 4.2.

_t_

0

_t_

1

_t_

2

_t_

3

_S_

?

_Sd_

?

_Su_

?

_Sd_

2

?

_S_

?

_Su_

2

?

_Sd_

3

_c_

_d_

3

max

(

\=

_Sd_

3

_K_

,0)

_Sd_

_c_

_ud_

2

\=

max

(

_Sd_

_K_

,0)

_Su_

_c_

_u_

2

_d_

\=

max

(

_Su_

_K_

,0)

_Su_

3

_c_

_u_

3

max

\=

(

_Su_

3

_K_

,0)

time

Figure 4.2: Payoff of a call in a 3-step tree.

Then call values are obtained walking the backward tree and applying the martingale property.

Figure 4.3: Backward induction in a 3-step tree.

**Example 4.2** _The current value of the ABC stock is 100. The volatility of its returns is estimated at 30%. The risk-free rate is 5%. Our goal is to value European and American puts written on ABC with exercise price of 102 and expiration of three months. To this end, we use a binomial tree with four steps._

134.99

The CRR tree parameters are given by

_u_

\=1

_._

0779

,

_d_

\=0

_._

and

9277

_q_

\=0

_._

. The dynamics of the

5021

UA leads to the following tree

_t_

0

_t_

1

_t_

2

_t_

3

_t_

4

time

100.00

92.77

107.79

86.07

100.00

116.18

79.85

92.77

107.79

125.23

74.08

86.07

100.00

116.18

Figure 4.4: UA in example 4.2.

The backward induction applied to the European put yields the top values in Figure 4.5. Hence

_p_(0_<sub>,</sub>_3_<sub>/</sub>_12_<sub>,</sub>_102) _≃_ 6_<sub>.</sub>_33_<sub>.</sub>_

Note that the value of the European option can be written directly. More precisely, for the European put we have

_N_ !

_p_(0_,T,K_) = _e−rT_ Xmax_K − SujdN−j_ _N qj_ (1 _− q_)_N−j , j j_\=0

where _<sub>N</sub>_ is number of steps in the tree and _<sub>j</sub>_ \= 0_<sub>,...,N</sub>_ represents the position of the UA in the tree (indexed starting from the bottom of the tree). It follows that, for every _<sub>j</sub>_, the terminal cash flow of the put is given by max_<sub>K − Su</sub><sup>j</sup><sub>d</sub><sup>N−j</sup>_. A necessary condition for the UA to end at the node _<sub>j</sub>_ at expiration is that the UA moves up _<sub>j</sub>_ times and moves down _<sub>N − j</sub>_ times which happen with probability _q<sup>j</sup>_ (1 _<sub>− q</sub>_)_<sup>N−j</sup>_. To know the number of all the paths that lead the UA to the position _<sub>j</sub>_ at expiration, it is

_t_

0

_t_

1

_t_

2

_t_

3

_t_

4

6.33

6.57

10.05

10.45

2.69

2.77

15.29

\[15.93\]

4.92

5.08

0.49

0.49

21.83

\[22.15\]

8.91

\[9.23\]

0.99

0.99

0.00

0.00

27.92

\[27.92\]

15.93

\[15.93\]

2.00

\[2.00\]

0.00

0.00

0.00

0.00

time

Figure 4.5: Values of the European (top) and American (bottom) puts in example 4.2. The value of the American put is within brackets when it is exercised. important to count all the possibilities of _<sub>j</sub>_ upward moves in a total _<sub>N</sub>_ moves. This number is given by _<sup>N</sup>j_ \= _N_!_/_(_j_!(_N − j_)!)_._

For the American put, every node of the tree should be compared to the intrinsic value of the option. Whenever the intrinsic value is larger than the continuation value, the owner of the put would exercise; the values in brackets in Figure 4.5 highlight cases when the exercise value replaced the American put’s continuation value. We have

_P_ (0_,_3_/_12_,_102) _≃_ 6_._57 _\> p_(0_,_3_/_12_,_102)_._

Note that the continuation value of _<sub>P</sub>_ is greater at _<sub>t</sub>_<sub>1</sub> (or at _<sub>t</sub>_<sub>2</sub> when _<sub>S</sub>_(_<sub>t</sub>_<sub>2</sub>) = _<sub>S</sub>_<sub>0</sub>) even if the put is not exercised. At each point in time, the continuation value of the American put is obtained from the martingale property applied on future values of the _American_ put: the option to early exercise in the future has value even when immediate exercise does not. The fact that the American and European values are the same in some upper nodes for _<sub>tn < T</sub>_ illustrates that when <sub>∆</sub>_<sub>t</sub>_ is not small enough, the binomial tree will not be rich enough to properly describe the dynamics of the derivatives.

### 4.1.4 Convergence of the CRR tree to the BMS model

The binomial model of Cox, Ross and Rubinstein converges to the log normal dynamics of the UA as the number of steps tends to infinity and the parameters _<sub>u</sub>_ and _<sub>d</sub>_ are adequately adjusted.

Denote by <sub>e</sub>_<sub>j</sub>_ (_<sub>n</sub>_) the random variable that counts the numbers of upside movement of the UA between _t_<sub>0</sub> \= 0 and _<sub>tn</sub>_. The value of the UA thus writes as

_S_ (_t<sub>n</sub>_) = _S · u_e_j_(_n_) _· dn−_e_j_(_n_)_._

According to the BMS model, the returns are Gaussian at all horizons. Let us study the variable ln _<sup>S</sup>_<sup>(</sup>_<sub>S</sub><sup>tn</sup>_<sup>)</sup>.

ln _<sup>S</sup>_ <sup>(</sup>_<sup>tn</sup>_<sup>)</sup> \= <sub>e</sub>_j_ (_n_)ln_u_ \+ _n −_ <sub>e</sub>_j_ (_n_)ln_d_

_S_

\= <sub>e</sub>_<sub>j</sub>_ (_n_)ln _<sup>u</sup>_ \+ _n_ln_d._ (4.1) _d_

We define the counting random variable <sup>n</sup>_<sub>Z</sub>_<sub>e</sub>_<sub>i</sub>_<sup>o</sup> such that

_i≥_0 _Z_e_i_ \= 10 if the UA moves up atif the UA moves down at_ti_ (_ti_probability(probability_p_)_,_1 _− p_)_._ (

We thus obtain

_n_

e_j_ (_n_) = <sup>X</sup>_Z_<sub>e</sub>_<sub>i</sub>._

_i_\=1

Since the variables _<sub>Z</sub>_<sub>e</sub>_<sub>i</sub>_ are independent and identically distributed, the central limit theorem implies that, as _<sub>n</sub>_ tends to infinity, <sub>e</sub>_<sub>j</sub>_ (_<sub>n</sub>_) is a Gaussian variable with moments given by

|     |     |
| --- | --- |
| E he_j_ (_n_)i | \= _np,_ |
| Var <sub>e</sub>_j_ (_n_)<br><br>As a consequence, when _<sub>n</sub>_ is large enough, we get | \= _np_(1 _− p_)_._ |
|     | q   |

e_j_ (_n_) _∼ N np_; _np_(1 _− p_) _,_

and using equation (4.1), the UA returns converge to

ln _S_ (_tn_) _∼ N np_ln _u_ \+ _n_ln_d_;ln _u_q_np_(1 _− p_)_._

_S d d_

Therefore, to be compatible with the BMS model, it is necessary to have

 h _S_(_tn_)i = _µtn_

E ln _SS_(_tn_) = _σ_2_tn_ (4.2) Var ln

 _S_

Setting, as suggested by Cox et al. (1979),

_u_ \= exp _σ_r_tn_ ! = <sup>1</sup>_<sub>,</sub> n d_

we obtain the following sufficient condition for the system of equations (4.2) to hold

_n_

_p_

_≃_

_µ_

p

_t_

_n_

_/n_

+

_σ_

2

_σ_

_._

Indeed :

E

ln

_S_

(

_t_

_n_

)

_S_

\=

_n_

_µ_

q

_t_

_n_

_n_

+

_σ_

2

_σ_

2

_σ_

r

_t_

_n_

_−_

_nσ_

r

_t_

_n_

_n_

\=

_µt_

_n_

_,_

|     |     |     |     |
| --- | --- | --- | --- |
| and |     |     |     |
|     | Var ln _S_ (_tn_)<br><br>_S_ | \=  | _t µ tn_ \+ _σ σ − µ_q_tn_ q<br><br>4 2 _n_ 2_n_ 2 _n σ n_<br><br>_n σ σ_ |

\= _σ_2_tn − µ_2 _t_2_n_ \= _σ_2_tn − µ_2_n_∆_t_2_. n_

In particular, the variance converges to _<sub>σ</sub>_<sup>2</sup>_<sub>tn</sub>_, but asymptotically only, as <sub>∆</sub>_<sub>t</sub>_<sup>2</sup> converges to 0 faster than _<sub>n</sub>_ to infinity.

For a European option, the central consideration is that the terminal distribution (i.e., at _<sub>tN</sub>_ \= _<sub>T</sub>_) converges to that of the BMS model. Consider a European call with exercise price of 80, and expiration of one year. The current value of the UA is 100 and the returns volatility is 20%. The risk-free rate is 5%. The BMS price is approximately 24.59 and the prices implied by the CRR tree are graphed on the following figure for trees with number of steps _<sub>N</sub>_ \= 2_<sub>,...,</sub>_100:

0

20

40

60

80

100

N

24.45

24.50

24.55

24.60

24.65

24.70

24.75

Price

BMS price

Figure 4.6: European call price, obtained from N-step trees, _<sub>N</sub>_ \= 2_<sub>,...,</sub>_100.

For small values of _<sub>N</sub>_, the error is very large. As _<sub>N</sub>_ grows, it appears that the binomial model converges slowly and non-smoothly to the BMS price with a bias in general. However, for an at-the-money option, this convergence is almost unbiased. This remark allows to use the following trick to speed up the convergence. A more precise result could be obtained by computing the CRR prices for two trees with _<sub>N</sub>_ and _<sub>N</sub>_ \+ 1 steps respectively and by taking the average of the two prices. The following numerical example illustrates this point.

**Example 4.3** _Consider a put with expiration in three months, a strike of 102 written on an UA which trades at 100 and which has a volatility of 30%. Moreover, the risk-free rate is 5%. Its BMS price is given by_

_p<sub>BMS</sub>_ (0_,_3_/_12_,_102) = 6_._37401127_._

_Using the binomial method, one obtains_

(_p<sub>CRR</sub>_ (_N_ \= 500) + _p<sub>CRR</sub>_ (_N_ \= 501)) = 6_._3742_,_

_which corresponds to a better precision (and a shorter computation time) than_

_p<sub>CRR</sub>_ (_N_ \= 1000) = 6_._37343_._

### 4.1.5 The Jarrow and Rudd parametrization

The use of the binomial model as proposed by Cox et al. (1979) highlights that the convergence to the BMS model is not a problem with a unique solution. In particular, the selected parameters _<sub>u</sub>_ and _<sub>d</sub>_ implies that risk-neutral probability is 0.5 only in the limit. Jarrow and Rudd (1983) proposes an alternative parametrization to the CRR tree. They suggest to use the following parametrization

#

_ut ,_

#

_dt , q_ \= 0_._5_._

In this specification, the risk-neutral probability is set at 0.5. In addition, parameters _<sub>u</sub>_ and _<sub>d</sub>_ result from the discretization of the GBM dynamics. In particular, they incorporate both the drift and the volatility of the UA returns.

### 4.1.6 Convergence improvements

Leisen and Reimer (1996) prove that the convergence to BMS model is faster when one node of the binomial tree corresponds to the exercise price at expiration. In order words, the tree should be constructed in such a way that

_K_ \= _S<sub>j</sub>_ (_T_)_,_

for a given _<sub>j</sub>_ which represents the position of the node _<sub>S</sub>_ in the tree. More generally, Widdicks et al. (2002) show that the quality of the convergence (particularly the possibility of monotonic convergence) depends on the distance between _<sub>K</sub>_ and the value of the UA at the node above the one corresponding to _<sub>K</sub>_.

Tian (1999) proposes a binomial tree with a perturbation parameter where the factors _<sub>u</sub>_ and _<sub>d</sub>_ are given by

 _ut ,_

_d_ _._

The _<sub>λ</sub>_ parameter allows to adjust the tree upward or downward. Tian (1999) shows that a proper choice of _<sub>λ</sub>_ can improve the convergence of the tree (particularly for a monotonic convergence to the BMS price).

For American options, Broadie and Detemple (1996) prove that the convergence of the binomial method can be improved when the pricing algorithm is not initiated at terminal date _<sub>T</sub>_ but at the next to last date _t<sub>N−</sub>_<sub>1</sub> \= _<sub>T −</sub>_ <sub>∆</sub>_<sub>t</sub>_ using the BMS values of the European option with the same characteristics and maturity

∆_t_.

Finally, the convergence improves when the binomial method is more accurate at the nodes of the tree that account for the convexity of the options prices (that is within an area that surrounds the exercise price). For American options, it is also desirable to have a tree that is more accurate for the nodes that are close to the expiration. Using this idea, Figlewski and Gao (1999) develop a binomial or adaptive trinomial model (“adaptive mesh model”). The step of this model can be modified depending on whether the UA is close to the exercise price or close to expiration. In this tree, the backward induction algorithm remains the same with the only exception that the level of discretization of the tree can be increased in areas where it leads to a significant improvement of the accuracy of the price.

## 4.2 Expanded binomial trees

Rubinstein (1994, 1998) adjusts the standard binomial tree to account for the non-Gaussian distribution of the UA returns. Let _<sub>b</sub>_(_<sub>n,j</sub>_) denote the binomial law density

(_n,j_) =_j_!(_<sub>n</sub>n<sub>−</sub>_! _<sub>j</sub>_)!_. b_

Discretizing space into _<sub>n</sub>_ \+ 1 points, the binomial distribution can be represented by a random variable _<sub>x</sub>_ taking the value

_x_ \= _x_(_n,j_) = 2_j~~√~~− n, n_

with probability _<sub>b</sub>_(_<sub>n,j</sub>_) for _<sub>j</sub>_ going from 0 to _<sub>n</sub>_. Let _<sub>ξ</sub>_ and _<sub>κ</sub>_ denote the skewness and kurtosis coefficients for the UA returns. Rubinstein (1998) suggests using an Edgeworth expansion to obtain an approximation for _<sub>ϕ</sub>_(_<sub>n,j</sub>_), the density of UA returns _<sub>ϕ</sub>_(_<sub>n,j</sub>_) = _<sub>b</sub>_(_<sub>n,j</sub>_) 1 + _ξ x_<sup>3</sup>6_−_ 3_x_ \+ (_κ −_ 3) _x_<sup>4</sup>24_−_ 6_x_<sup>2</sup> \+ 3 \+ _ξ_<sup>2</sup> _x_<sup>5</sup> _−_ 1072_x_<sup>3</sup> \+ 15_x_<sup>!</sup>_<sub>.</sub>_

That density does not exactly sum up to one and must therefore be normalized to obtain

_f_ (_n,j_) = P_nuϕ_\=0(_n,jϕ_(_<sub>n,u</sub>_) )_._

The value of the European call is then given by

<sup>X</sup>_N_ h n _√_ o _c_(0_,T,K_) = _e<sup>−rT</sup> f_ (_N,u_)max 0_,S_ exp _µT_ \+ _σ TY_ (_N,u_) _− K_<sup>i</sup>

_u_\=0 where

_µ_ \= _r − y −_ 1 ln X_N f_(_N,u_)expn_σ√TY_ (_N,u_)o!_,_

_T_

_u_\=0 and _<sub>Y</sub>_ (_<sub>n,u</sub>_) is the standardized UA returns density, i.e.

(_n,j_) = _x_(_n,j_<sub>p</sub>) _− M_ (_n_)_,_

_Y_

_V_ ~~(~~_n_~~)~~

with

_n_

_M_ (_n_) = <sup>X</sup> _f_ (_n,u_)_x_(_n,u_)_,_

_u_\=0 _n_

_V_ (_n_) = <sup>X</sup> _f_ (_n,u_)(_x_(_n,u_) _− M_ (_n_))<sup>2</sup> _._

_u_\=0

This approach is interesting for pricing options written on UA whose returns depart from normality only slightly. Indeed, for large (absolute) skewness or kurtosis, the Edgeworth expansion may lead to multimodal distributions and also negative probabilities. Simonato (2011) proposes to expand the binomial tree with Johnson distributions, which circumvents the limitations mentioned above.

## 4.3 Trinomial trees

To accelerate the convergence of the tree method to the continuous time solution, one can resort to the trinomial tree. Boyle (1986) develops a trinomial tree where the UA does not change in its central node.

For each date _<sub>tn</sub>_ \+ ∆_<sub>t</sub>_, the UA takes on the values _<sub>uS</sub>_(_<sub>tn</sub>_), _<sub>mS</sub>_(_<sub>tn</sub>_) and _<sub>dS</sub>_(_<sub>tn</sub>_) with

_ut, m_ \= 1_, dt,_

and the risk-neutral probabilities corresponding to the increase, stagnation and decrease of the UA are

respectively given by

|     |     |     |
| --- | --- | --- |
| _qu_<br><br>_qm_ | \=<br><br>\= | 2_λ_1<sup>2</sup> \+ 2_λσ_<sup>2</sup> _<sup>,</sup>_<br><br>1 _−_ 12 _,_ |

_σ_2

_r − y −_ ∆_t_

_<sub>λ</sub>_

_q<sub>d</sub>_ \= 2_λ_12 _− r − y_2_−λσσ_22 ∆_t._

The _<sub>λ</sub>_ parameter should be chosen as to obtain the fastest possible convergence. Using some experimentations, Boyle (1986) finds that the best results are obtained when the three risk-neutral probabilities are approximately equal, which is obtained for _<sub>λ</sub>_ close to 1.2.

In its most general form, a trinomial tree involves six parameters: the increase, stagnation and decrease of the UA factors (denoted _<sub>u</sub>_, _<sub>m</sub>_ and _<sub>d</sub>_ respectively) and the risk-neutral probability attached to these events

(denoted _<sub>qu</sub>_, _<sub>qm</sub>_ and _<sub>qd</sub>_ respectively). To ensure the convergence of this trinomial tree to the BMS solution,

|     |     |     |
| --- | --- | --- |
|     | _q<sub>u</sub>_ \+ _q<sub>m</sub>_ \+ _q<sub>d</sub>_ \= | 1_,_ |
|     | _q<sub>u</sub>u_ \+ _q<sub>m</sub>m_ \+ _q<sub>d</sub>d_ \= | _M,_ |
| with | _quu_2 + _qmm_2 + _qdd_2 =<br><br>E<sup>Q</sup> \[_S_ (∆_t_)\] | _V,_ |

Tian (1993) proves that these parameters should fulfill the following conditions

_M_ \= = exp_{_(_r − y_)∆_t},_

_S_

_V_ \= E 2 _σ_2∆_t_o_._

_S_

Moreover, to ensure that the intermediate nodes recombine, we should have

_ud_ \= _m_<sup>2</sup>.

This specification allows to reduce the number of values of the UA at the last node _<sub>N</sub>_ to 2_<sub>N</sub>_ +1. Therefore, we are left with four equations to infer the six parameters. Note in particular the Boyle (1986)’s choice of setting _<sub>m</sub>_ \= 1 and _<sub>u</sub>_. Tian (1993) suggests to obtain the two missing conditions by resorting to the third and fourth moments of the UA distribution. By doing so, we can achieve the

convergence to the BMS model by setting

_u_ \= _H_ \+ <sup>p</sup>_H_<sup>2</sup> _− m_<sup>2</sup>_,_

|     |     |     |
| --- | --- | --- |
| where _H_ \= <sub>2</sub>_<sup>mV</sup><sub>M</sub>_2 (_V_ \+ 1), and |     | _m_ <sup>\=</sup> _M_<sub>3</sub> _, d_ \= _H −_ <sup>p</sup>_H_<sup>2</sup> _− m_<sup>2</sup>_,_ |
| _qu_ | \=  | _md − M_ (_m_ \+ _d_) + _V_<br><br>(_u − d_)(_u − m_) _<sup>,</sup>_ |
| _qm_ | \=  | _M_ (_u_ \+ _d_) _− ud − V_<br><br>(_u − m_)(_m − d_) _<sup>,</sup>_ |
| _q<sub>d</sub>_ | \=  | _um − M_ (_u_ \+ _m_) + _V_<br><br>( )( ) _<sup>.</sup>_ |

_V_ 2

_u − d m − d_

## 4.4 Replication

The option seller receives a small initial gain (the premium) and is then exposed to a potentially considerable loss (up to the strike for a short put position, unlimited for a short call position). To hedge against this risk, the option seller can hardly rely on an insurance strategy, in part because the risks related to various short positions in options are strongly correlated between each other. This hedging problem has long stood as a serious obstacle to a profitable and sustainable option selling activity and thereby to the development of options markets.

Beyond their pricing model, the seminal contribution of Black and Scholes (1973) is the identification of a hedging strategy. For each option sold, it is possible under the BMS framework to build a self-financing portfolio that perfectly replicates the short position in the option. In other words, no matter the evolution of the UA price, the replicating portfolio can exactly match the value of the option sold. To make a profit, the option seller just needs to price the option at the cost of the replicating portfolio plus a margin.

In practice, it is impossible to implement the BMS replicating strategy for at least two major reasons: (i) Portfolio rebalancing cannot be executed in continuous time, and it looks more realistic to study the hedging problem in discrete time, (ii) portfolio rebalancing is associated with transaction costs and if they are not properly anticipated, they could wipe out the margin collected initially when selling the option. In this section, we address these two issues and present solutions to improve the quality of imperfect replication. These solutions consist in managing option price sensitivities to the major factors affecting them. These sensitivities are known as Greek parameters, or simply Greeks.

On top of the two issues mentioned above comes model risk, i.e. the fact that the replication strategy could yield very poor results simply because the option seller is not relying on an accurate description of the UA price dynamics. To cope with model risk, we will present in subsequent chapters extensions of the BMS framework. Under these more sophisticated models, replication strategies can be implemented in the same fashion as described below. The definition and management of Greeks still holds under any pricing framework. The chosen model will only change the computation of the Greeks.

### 4.4.1 Greek parameters

Greeks are price sensitivities calculated as partial derivatives with respect to some specific factors. Since the partial derivative is a linear operator, the Greek parameter of a total position is simply the weighted sum of the Greeks of the individual positions, that is, for any Greek Ψ

Ψportfolio = X_ni_Ψ_i,_

_i_

where _<sub>ni</sub>_ denotes the position in asset _<sub>i</sub>_.

In analytical models like the BMS framework, Greeks can be expressed analytically. In tree models or in other numerical approaches, Greeks will be approximated.

##### The delta neutral position

Intuitively, the most important determinant of the value of a derivative is the underlying asset price. The delta measures that sensitivity<sup><sup>[\[5\]](#footnote-5)</sup></sup>

∆_g_ \= _dg <sub>.</sub> dS_

In the diffusion model, Merton (1973) and Jagannathan (1984) prove that the call (put) option premium is an increasing (decreasing) function of the underlying asset price. Therefore, the delta of vanilla calls and puts are such that

0 _<_ ∆_<sub>C</sub> <_ 1_, −_1 _<_ ∆_<sub>P</sub> <_ 0_,_

and, because of put-call parity, European options further verify

∆_<sub>c</sub> −_ ∆_<sub>p</sub>_ \= ∆_<sub>S</sub>_ \= 1_._

Albeit intuitive, this property may not hold for discontinuous underlying asset price processes or for some asset volatility specifications. Bergman et al. (1996) study this question more in depth.

BMS deltas for the European call and put are

∆_BMS<sub>c</sub>_ _,_

∆_BMSp_ \= _∂pBMS_ \= _−e−yT_ Φ(_−d_1)_._

_∂S_

In the CRR tree, deltas can be computed as follows

_c − c<sub>d</sub> u − d_)_<sup>,</sup>_

∆

_CRR_

_c_

_≃_

_u_

_S_

(

∆

_CRR_

_p_

_≃_

_S_

_pu − pd_

(_u − d_)_<sup>.</sup>_

The most basic replication strategy consists in forming a delta neutral portfolio. This approach is commonly referred to as delta hedging. By definition, such a position should be little affected by small UA price variations.

In the continuous-time BMS framework, we proved, by means of Itˆo’s lemma and the AoA, that delta hedging implies perfect replication. We now illustrate the limits of delta hedging when portfolio rebalancing occurs in discrete time.

Suppose we are short of one European call. To simplify the exposition, assume the UA pays no dividends (_<sub>y</sub>_ \= 0). According to BMS, the delta of our position is _<sub>−</sub>_Φ(_<sub>d</sub>_<sub>1</sub>). To achieve a delta neutral position, we need to buy Φ(_<sub>d</sub>_<sub>1</sub>) units of the UA using the proceeds from the sale of the call and borrowing the remainder

(to keep a self-financing strategy). Formally, the value of our portfolio is given by

_V_ \= _−c_(_t,T,K_) + Φ(_d_<sub>1</sub>)_S_(_t_) _−_ Φ(_d_<sub>1</sub>)_S_(_t_) _− c_(_t,T,K_) \= 0_._

short call UA position amount borrowed

Our total position is the sum of our initial position (short one call) and the replicating, or hedging, portfolio whose goal is to track the value of the call as closely as possible. In _<sub>δt</sub>_ units of time later, our total position is worth

_V_ \+ _δV_ \= _−c_(_t_ \+ _δt,T,K_) + Φ(_d_<sub>1</sub>)_S_(_t_ \+ _δt_) _−_ Φ(_<sup>d</sup>_<sup>1</sup>)_<sup>S</sup>B_(_<sup>t</sup>_)(0_<sup>−</sup><sub>,δt</sub><sup>c</sup>_()_<sup>t,T,K</sup>_)_<sub>.</sub>_

We now develop a numerical example to assess the magnitude of _<sub>δV</sub>_ . Assume the following data:

_S T K r σ_

100 1 100 0.05 0.2

According to the BMS model,

_c_(0_<sub>,</sub>_1_<sub>,</sub>_100) = 10_<sub>.</sub>_4506_<sub>,</sub>_ Φ(_<sub>d</sub>_<sub>1</sub>) = 0_<sub>.</sub>_6368_<sub>.</sub>_

At initial date, we sell 10 1-year, ATM European calls, each call being written on 100 units of UA. This yields a cash inflow of $10,451. The hedging portfolio is made of a long position in 637 units of UA, which costs $63,700. The self-financing constraint requires that we borrow 63700_<sub>−</sub>_10451 = 53249, that is, $53,249.

On the next day, the position on the loan is

_−_53249(1 + 0_<sub>.</sub>_05_<sub>/</sub>_360) _≃ −_53256_<sub>.</sub>_

The long position on the UA is _<sub>S</sub>_(_<sub>t</sub>_ \+ _<sub>δt</sub>_) _<sub>×</sub>_ 637, and the short position on calls is _<sub>−</sub>_1000_<sub>c</sub>_(_<sub>t</sub>_ \+ _<sub>δt,</sub>_1_<sub>,</sub>_100). The table below reports the net position according to various changes in UA price _<sub>S</sub>_(_<sub>t</sub>_ \+ _<sub>δt</sub>_).

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| _S_(_t_ + | _δt_) | Loan | Long in UA | Short in calls | Net position |
| 90  |     | _−_$53_<sub>,</sub>_256 | +$57_<sub>,</sub>_330 | _−_$5_<sub>,</sub>_077 | _−_$1_<sub>,</sub>_003 |
| 95  |     | _−_$53_<sub>,</sub>_256 | +$60_<sub>,</sub>_515 | _−_$7_<sub>,</sub>_495 | _−_$236 |
| 98  |     | _−_$53_<sub>,</sub>_256 | +$62_<sub>,</sub>_426 | _−_$9_<sub>,</sub>_198 | _−_$28 |
| 100 |     | _−_$53_<sub>,</sub>_256 | +$63_<sub>,</sub>_700 | _−_$10_<sub>,</sub>_433 | +$11 |
| 102 |     | _−_$53_<sub>,</sub>_256 | +$64_<sub>,</sub>_974 | _−_$11_<sub>,</sub>_743 | _−_$25 |
| 105 |     | _−_$53_<sub>,</sub>_256 | +$66_<sub>,</sub>_885 | _−_$13_<sub>,</sub>_840 | _−_$211 |
| 110 |     | _−_$53_<sub>,</sub>_256 | +$70_<sub>,</sub>_070 | _−_$17_<sub>,</sub>_645 | _−_$831 |

As expected, the performance of the local hedging strategy may look acceptable for small variations of the UA price, but it strongly deteriorates when the UA price varies substantially. It could become even worse if we considered changes in the risk-free rate or in the volatility as well.

##### The delta-gamma neutral position

A major limitation of the delta neutral hedging strategy stems from the fact that the delta changes during the hedging period. Continuous rebalancing allows to instantly adjust the position in the UA according to the evolution of delta. In practice, discrete rebalancing lets _<sub>δt</sub>_ units of time elapse before any correction in the UA position. Hedging is therefore no longer perfect.

One way to address this limitation is to account for the way delta varies with the UA price. Put differently, the net position should have a delta that is little affected by changes in _<sub>S</sub>_. This can be measured by the gamma

Γ_g_ \= _d_∆_g_ \= (_dg_)<sup>2</sup>2 _<sub>.</sub> dS_ (_dS_)

Since option payoffs are convex, the gamma of vanilla calls and puts are such that

0 _<_ Γ_<sub>C</sub>,_ 0 _<_ Γ_<sub>P</sub> ._

Because of put-call parity, the gamma of the European call and that of the European put are the same

Γ_<sub>c</sub>_ \= Γ_<sub>p</sub>._

In the BMS model, the European call or put gamma is given by

Γ_BMSc_ \= Γ_BMSp_ \= _∂_2_cBMS_2 = _∂_2_∂SpBMS_2 = _e−yT Sσϕ_(_~~√~~d_1_T_) _\>_ 0_._

_∂S_

In the CRR tree, one way to compute gamma is to discretize the second order partial derivative with

respect to the UA price, which yields

Γ_CRR<sub>c</sub>_ \=

_cuu −_ 2_cud_ \+ _cdd_

\[(_u − d_)_S_\]<sup>2</sup> _<sup>,</sup>_

Γ_CRR<sub>p</sub>_ \= _puu −_ 2_pud_ +<sup>2</sup>_pdd <sup>.</sup>_ \[(_u − d_)_S_\]

A better approximation of gamma consists in expressing it as the first order partial derivative with respect to delta, as illustrated in Figure 4.7. Hence,

(_guu−gud_) (_gud−gdd_)

Γ = ∆_S_(_uu−−_∆_dd_) = _u_2_S−SuS −− SdS−d_2_S ._

_t_

0

_t_

1

_t_

2

_t_

3

\=

_u_

_d_

_Su_

_Sd_

_Sd_

_d_

\=

_g_

_ud_

_g_

_d_

2

_S_

_Sd_

2

_Su_

_u_

\=

_g_

_u_

2

_g_

_ud_

_Su_

2

_S_

_Sd_

2

_g_

_d_

2

_S_

_g_

_ud_

_Su_

2

_g_

_u_

2

time

Figure 4.7: CRR Gamma. To build a delta-gamma neutral position, the replicating portfolio must contain the UA but also a non-linear derivative to manage gamma. Suppose we wish to hedge a position of _<sub>ng</sub>_<sub>1</sub> units of derivative _<sub>g</sub>_<sub>1</sub>.

To identify the replication strategy, we must solve the following three unknowns, three equations system

 0 = _ng_1_g_1 + _ng_2_g_2 + _nSS_ \+ _nBB,_



0 = _ng_ ∆_g_ \+ _ng_ ∆_g_ \+ _nS,_

 0 = _ng_11Γ_g_11+ _ng_22Γ_g_22_._ The first equation accounts for the self-financing constraint. The second and third equations result from imposing delta and gamma neutrality on our net position. Since _<sub>ng</sub>_<sub>1</sub> is known (it is the position to hedge), solving the system above yields _<sub>ng</sub>_<sub>2</sub> (from the gamma neutrality condition), then _<sub>nS</sub>_ (from the delta neutrality condition), and finally _<sub>nB</sub>_ (from the self-financing constraint).

To assess how managing the gamma may improve the quality of replication, we return to the same numerical example. Suppose we choose to include the 2-year, ATM European call. According to the BMS model,

1-year ATM call 2-year ATM call

|     |     |     |
| --- | --- | --- |
| Premium | 10_<sub>.</sub>_4506 | 16_<sub>.</sub>_1268 |
| Delta | 0_<sub>.</sub>_6368 | 0_<sub>.</sub>_6897 |
| Gamma | 0_<sub>.</sub>_0188 | 0_<sub>.</sub>_0125 |

Recall the sale of ten 1-year ATM European calls earns $10,451.

To be gamma neutral, we set

_n<sub>c</sub>_<sub>2</sub> \=  = 15_._04_,_

that is, we buy 15 2-year ATM European calls, which costs

15 _×_ 100 _×_ 16_<sub>.</sub>_1268 _≃_ 24190_<sub>,</sub>_ i.e. $24,190.

To be delta neutral, we set

_n<sub>S</sub>_ \= 1000 _×_ 0_<sub>.</sub>_6368 _−_ 1500 _×_ 0_<sub>.</sub>_6897 = _−_397_<sub>.</sub>_75_<sub>.</sub>_

We therefore sell 398 units of the UA and receive $39,800.

Applying the self-financing constraint, we lend the cash surplus:

10451 _<sub>−</sub>_ 24190 + 39800 = 26061_<sub>,</sub>_

that is, $26,061.

On the next day our lending position is worth

26061(1 + 0_<sub>.</sub>_05_<sub>/</sub>_360) _<sub>≃</sub>_ 26065_<sub>.</sub>_

The following table reports the net position according to various values of the UA price at _<sub>t</sub>_ \+ _<sub>δt</sub>_.

|     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- |
| _S_(_t_ + | _δt_) | Loan | Long in UA | Long calls _<sub>c</sub>_<sub>2</sub> | Short calls _<sub>c</sub>_<sub>1</sub> | Net position |
| 90  |     | +$26_<sub>,</sub>_065 | _−_$35_<sub>,</sub>_820 | +$14_<sub>,</sub>_845 | _−_$5_<sub>,</sub>_077 | _−_$13 |
| 95  |     | +$26_<sub>,</sub>_065 | _−_$37_<sub>,</sub>_810 | +$19_<sub>,</sub>_242 | _−_$7_<sub>,</sub>_495 | +$2 |
| 98  |     | +$26_<sub>,</sub>_065 | _−_$39_<sub>,</sub>_004 | +$22_<sub>,</sub>_138 | _−_$9_<sub>,</sub>_198 | +$1 |
| 100 |     | +$26_<sub>,</sub>_065 | _−_$39_<sub>,</sub>_800 | +$24_<sub>,</sub>_169 | _−_$10_<sub>,</sub>_433 | +$1 |
| 102 |     | +$26_<sub>,</sub>_065 | _−_$40_<sub>,</sub>_596 | +$26_<sub>,</sub>_275 | _−_$11_<sub>,</sub>_743 | +$1 |
| 105 |     | +$26_<sub>,</sub>_065 | _−_$41_<sub>,</sub>_790 | +$29_<sub>,</sub>_564 | _−_$13_<sub>,</sub>_840 | _−_$1 |
| 110 |     | +$26_<sub>,</sub>_065 | _−_$43_<sub>,</sub>_780 | +$35_<sub>,</sub>_363 | _−_$17_<sub>,</sub>_645 | +$3 |

The delta-gamma neutral strategy clearly outperforms the delta neutral strategy. Note that we have only considered variations in UA price, assuming once again that the risk-free rate and the volatility are unchanged.

##### Managing additional Greeks

More generally, a replication strategy might take into account more option premium determinants and therefore manage the corresponding Greeks accordingly. Consider the derivative _<sub>g</sub>_ whose value is a function of the UA price, time, the risk-free rate, the convenience yield, and the volatility

_g_ \= _g_ (_S,t,σ,r,y_)_._

Using a Taylor expansion and neglecting terms in (_<sub>δt</sub>_)<sup>2</sup> _<sub>,</sub>_(_<sub>δσ</sub>_)<sup>2</sup> and (_<sub>δr</sub>_)<sup>2</sup> (considering these are very small increments), we obtain

_δg__δy._

In the case of currency derivatives, hedging the foreign risk-free rate (_<sub>y</sub>_) is as important as hedging the domestic risk-free rate (_<sub>r</sub>_) (see Melino and Turnbull (1995)).

Let theta (_<sub>θg</sub>_), vega (_<sub>ϑg</sub>_), rho (_<sub>ρg</sub>_) and epsilon (_<sub>ϵg</sub>_) denote the partial derivatives of _<sub>g</sub>_ with respect to time, volatility, risk-free rate and convenience yield, respectively. In continuous time, the former approximation can be rewritten as

_dg_ _ϵ<sub>g</sub>dy._

In the BMS model, these additional Greeks are given by

 _rKe<sup>−rT</sup>_ Φ(_d_<sub>2</sub>) + _ySe<sup>−yT</sup>_ Φ(_d_<sub>1</sub>)_,_

_θ<sub>p</sub>rKe<sup>−rT</sup>_ Φ(_−d_<sub>2</sub>) _− ySe<sup>−yT</sup>_ Φ(_−d_<sub>1</sub>)_,_

_√_

_ϑ<sub>c</sub>_ \= _ϑ<sub>p</sub>_ \= _e<sup>−yT</sup> S Tϕ_(_d_<sub>1</sub>)_,_

_ρ<sub>c</sub>_ \= _TKe<sup>−rT</sup>_ Φ(_d_<sub>2</sub>)_, ρ<sub>p</sub>_ \= _−TKe<sup>−rT</sup>_ Φ(_−d_<sub>2</sub>)_, ϵ<sub>c</sub>_ \= _−TSe<sup>−yT</sup>_ Φ(_d_<sub>1</sub>)_, ϵ<sub>p</sub>_ \= _TSe<sup>−yT</sup>_ Φ(_−d_<sub>1</sub>)_._

**Lemma 4.4** _In the one-dimensional diffusion model, a delta-gamma neutral, self-financed position is also theta neutral._

**Proof** Recall the fundamental PDE that holds when the UA price is driven by a one-dimensional

diffusion

 _rg,_

or, using Greek parameters,

 _rg._

For a delta-gamma neutral position,

_θ<sub>g</sub>_ \= _rg_ \= 0_,_

where the last equality stems from the self-financing condition.□

Put differently, the above lemma states that, under the BMS setup once the position is delta neutral, it is equivalent to manage the gamma or the theta. Such equivalence may no longer hold of course, if the UA price dynamics is more complex than a one-dimensional diffusion.

In practice, priority is given to managing the vega since volatility appears to be a major driver of option premiums. The rho and epsilon sensitivities are often neglected as interest rate or convenience yield variations have little impact on option values, especially when option maturity is short. Admittedly, this may no longer be the case for foreign exchange or commodity derivatives.

In sum, the choice of which Greeks to manage must be made wisely. All else equal, one should expect that a replication strategy involving more Greeks should improve its hedging performance. There are at least two limits to this line of reasoning. First, any additional Greek under management requires that the hedging portfolio include one more derivative, which induces higher transaction costs. Second, any additional Greek under management increases the replication strategy’s exposure to model risk. If the dynamics of the UA price are not properly captured, then all Greeks are computed with some imprecision, and as a consequence hedging errors might accumulate.

In what follows, we extend the preceding replication strategy to manage vega risk. Two non-linear derivatives are now required in the hedging portfolio to ensure both gamma and vega neutrality. This leads to a system of four equations with four unknowns as shown below:

 0 = _ng_1_g_1 + _ng_2_g_2 + _ng_3_g_3 + _nSS_ \+ _nBB,_

 0 = _ng_1∆_g_1 + _ng_2∆_g_2 + _ng_3∆_g_3 + _nS,_  0 = _ngg_11_ϑgg_11 + _nngg_22_ϑ_Γ_gg_22 ++_nngg_33_ϑ_Γ_gg_33_.,_

0 = _n_ Γ +

Equations three and four must be solved jointly to determine the positions _<sub>ng</sub>_<sub>2</sub> and _<sub>ng</sub>_<sub>3</sub> (recall that _<sub>ng</sub>_<sub>1</sub> is given as the initial position to hedge). Then the second equation (delta neutrality) and the first equation (self-financing condition) are solved to obtain _<sub>nS</sub>_ and _<sub>nB</sub>_, respectively.

Back to the same numerical example, we choose to include the 2-year European call with strike 100 and the 1.5-year European call with strike 110 into the hedging portfolio. BMS calculations yield

1.5-year call with strike 110

|     |     |
| --- | --- |
| Premium | 8_<sub>.</sub>_8554 |
| Delta | 0_<sub>.</sub>_5158 |
| Gamma | 0_<sub>.</sub>_0163 |

and the three vegas are 0.3752 for the call to replicate, 0.4991 for the 2-year ATM call and 0.4882 for the 1.5-year call with strike 110. To determine the composition of the replicating portfolio, we solve the following system

 0 = _−_1000 _×_ 10_._4506 + _n<sub>c</sub>_<sub>2</sub>1612_._68 + _n<sub>c</sub>_<sub>3</sub>885_._54 + _n<sub>S</sub>_100 + _n<sub>B</sub>B,_  0 = _−_1000 _×_ 0_._6368 + _n<sub>c</sub>_<sub>2</sub>68_._97 + _n<sub>c</sub>_<sub>3</sub>51_._58 + _n<sub>S</sub>,_  0 = _−_1000 _×_ 0_._3752 + _n<sub>cc</sub>_<sub>22</sub>49_._25 +_._91 +_nn<sub>c</sub>_<sub>3</sub>_<sub>c</sub>_1<sub>3</sub>_._4863_.,_82_._

0 = _−_1000 _×_ 0_._0188 + _n_ 1

The solution yields the following strategy: Sell 15 calls _<sub>c</sub>_<sub>2</sub>, buy 23 calls _<sub>c</sub>_<sub>3</sub>, buy 485 units of the UA, and borrow $34,200.

The money market position on the next day is

_−_34200(1 + 0_<sub>.</sub>_05_<sub>/</sub>_360) _≃ −_34205_<sub>,</sub>_

that is, short of $34,205. The table below reports the net position according to various changes in UA price.

|     |     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- |
| _S_(_t_ + | _δt_) | Loan | Long in UA | Short calls _<sub>c</sub>_<sub>1</sub> | Short calls _<sub>c</sub>_<sub>2</sub> | Long calls _<sub>c</sub>_<sub>3</sub> | Net position |
| 90  |     | _−_$34_<sub>,</sub>_205 | +$43_<sub>,</sub>_650 | _−_$5_<sub>,</sub>_077 | _−_$14_<sub>,</sub>_845 | +$10_<sub>,</sub>_398 | _−_$79 |
| 95  |     | _−_$34_<sub>,</sub>_205 | +$46_<sub>,</sub>_075 | _−_$7_<sub>,</sub>_495 | _−_$19_<sub>,</sub>_242 | +$14_<sub>,</sub>_881 | +$14 |
| 98  |     | _−_$34_<sub>,</sub>_205 | +$47_<sub>,</sub>_530 | _−_$9_<sub>,</sub>_198 | _−_$22_<sub>,</sub>_138 | +$18_<sub>,</sub>_038 | +$27 |
| 100 |     | _−_$34_<sub>,</sub>_205 | +$48_<sub>,</sub>_500 | _−_$10_<sub>,</sub>_433 | _−_$24_<sub>,</sub>_169 | +$20_<sub>,</sub>_334 | +$27 |
| 102 |     | _−_$34_<sub>,</sub>_205 | +$49_<sub>,</sub>_470 | _−_$11_<sub>,</sub>_743 | _−_$26_<sub>,</sub>_275 | +$22_<sub>,</sub>_779 | +$26 |
| 105 |     | _−_$34_<sub>,</sub>_205 | +$50_<sub>,</sub>_925 | _−_$13_<sub>,</sub>_840 | _−_$29_<sub>,</sub>_564 | +$26_<sub>,</sub>_720 | +$36 |
| 110 |     | _−_$34_<sub>,</sub>_205 | +$53_<sub>,</sub>_350 | _−_$17_<sub>,</sub>_645 | _−_$35_<sub>,</sub>_363 | +$33_<sub>,</sub>_972 | +$109 |

The delta-gamma-vega neutral strategy seems to slightly underperform the delta-gamma neutral strategy. However, we have assumed that the volatility remained constant. The next table reports the net positions obtained from the two strategies for different UA price and volatility scenarios.

_σ_ \= 18% _<sub>σ</sub>_ \= 20% _<sub>σ</sub>_ \= 22%

_S_(_<sub>t</sub>_ \+ _<sub>δt</sub>_) ∆-Γ ∆-Γ-_<sub>ϑ</sub>_ ∆-Γ ∆-Γ-_<sub>ϑ</sub>_ ∆-Γ ∆-Γ-_<sub>ϑ</sub>_

~~90~~ _−_~~$796 +$291~~ _−_~~$13~~ _−_~~$79 +$814~~ _−_~~$404~~ 95 _<sub>−</sub>_$772 +$204 +$2 +$14 +$780 _<sub>−</sub>_$161 98 _<sub>−</sub>_$752 +$97 +$1 +$27 +$764 _<sub>−</sub>_$52 100 _<sub>−</sub>_$739 +$17 +$1 +$27 +$753 +$14 102 _<sub>−</sub>_$727 _<sub>−</sub>_$61 +$1 +$26 +$743 +$78

105 _<sub>−</sub>_$709 _<sub>−</sub>_$163 _<sub>−</sub>_$1 +$36 +$729 +$179

110 _<sub>−</sub>_$675 _<sub>−</sub>_$246 +$3 +$109 +$710 +$388

If volatility does not change, the delta-gamma neutral strategy clearly has an edge because it is designed as the best hedging strategy assuming only the UA price is variable (and not the volatility). The deltagamma-vega neutral strategy proves its superiority when the two sources of risk are combined.

### 4.4.2 Managing imperfect replication

##### Price adjustments

Under the BMS model, Boyle and Emanuel (1980) examine the delta-neutral strategy replicating a vanilla option. They show that the hedging error at each rebalancing date _<sub>t</sub>_ is a random variable that can be written as

12 _ε_2 _−_ 1_σ_2_S_2(_t_)Γ_δt._

Thus, the hedging error is centered and proportional to the option gamma, and follows a chi-square law with one degree of freedom.

In an options market where the financial institution (e.g. option seller) has all the bargaining power, it could charge the hedging error to the end-user (e.g. option buyer). Thus, the option premium would reflect an ex ante compensation for the exposure to imperfect replication. In this spirit, Wilmott (1994) works with a discrete time version of the BMS framework. Specifically, the UA price is driven by

_S_ \= exp(_<sub>x</sub>_)_<sub>,</sub>_

where

_x_ 

Wilmott (1994) shows that the premium of the European option can be adjusted to take imperfect replication into account. The adjustment can be expressed in terms of a modified volatility used as the revised input into the BMS pricing formula:

 _δt_

_._

_σ_

Again, assuming that the end-user pays entirely for the risk of imperfect hedging, then the modified volatility is adjusted upwardly (downwardly) when the option position to replicate is short (long).

Note that the volatility adjustment involves the UA price drift _<sub>µ</sub>_. Indeed, in the BMS framework, replication is perfect, which means it is possible to continuously rebalance a portfolio made of one unit short of the derivative and delta units long of the UA and obtain a risk-free position. In the AoA, such a portfolio must earn the risk-free rate. The value of the derivative is thereby related to _<sub>r</sub>_ and not related to _<sub>µ</sub>_. If that continuous rebalancing is no longer feasible, the risk-free portfolio cannot be constructed. In other words, within _<sub>δt</sub>_ units of time, the UA grows at rate _<sub>µ</sub>_ while the positions in the replicating portfolio are not updated. Hence the value of the derivative is impacted by _<sub>µ</sub>_.

Imperfect replication arises when rebalancing is not continuous but also when transactions are costly. Leland (1985) studies a discrete time version of the BMS framework. The UA price is driven by a discretized

GBM _<sub>√</sub>_

_δS_ \= _µSδt_ \+ _σS δtε,_

where _<sub>δt</sub>_ denotes the constant period of time between two trading / rebalancing dates. Transaction costs are assumed to be proportional to the UA price, that is buying (selling) _<sub>x</sub>_ units of the UA costs (earns) _κxS_ with _<sub>κ</sub>_ a scalar. In this framework, Leland (1985) shows that the European option can be valued with the BMS formula and the following volatility adjustment

_σ_ \= _σ_ 1 _± ._

_σ πδt_

Boyle and Vorst (1992) and Palmer (2001) extend Leland’s (1985) analysis in a binomial tree and obtain a similar volatility adjustment. Hoggard et al. (1994) show that this adjustment is only valid for positions with a gamma that keeps the same sign (like a vanilla option, unlike a spread for example).

##### Strategy selection

We have considered thus far that rebalancing occurs at fixed time intervals. Some authors have examined replication strategies with a different rebalancing criterion. For instance, Henrotte (1993), Toft (1996) or Martellini (2000) study strategies where the hedging portfolio is rebalanced as soon as the UA price or the delta has changed by a certain proportion. Other authors determine an endogenous hedging frequency by maximizing the investor’s utility function. For instance, Hodges and Neuberger (1989) and Davis et al. (1993) deal with an option seller with exponential utility facing proportional transaction costs. They find that the optimal delta-neutral strategy consists in maintaining the delta of the position within a band centered around the BMS delta.

Some studies perform horse races among various replication methods in the presence of transaction costs using real or simulated data (see e.g. Mohamed (1994), Wilmott (2000), or Martellini and Priaulet (2002)). These studies do not reach a consensus as to which strategies perform best. Toft (1996) proposes a mean-variance framework to select an optimal strategy. Each replication method (characterized by the Greeks under management and the rebalancing criterion) generates a hedging error net of transaction costs denoted by _<sub>H</sub>_. In the mean-variance space for _<sub>H</sub>_, the best strategy is the one displaying the closest to zero E \[_<sub>H</sub>_\] with the lowest Var (_<sub>H</sub>_).

## 4.5 Problem set

#### Exercise 4.1

The stock ABC trades at 122. Compute the values of the European and American call and put on this stock with exercise price at 120 using the CRR tree using the following information:

- the options have 6 months to expiration,
- the risk-free rate is 8%,
- there is no dividend,
- the number of steps is 3,
- the annualized return volatility is 25%.

Compute the delta and the gamma of the American options. Use two different methods for the gamma.

#### Exercise 4.2

Rework the questions of the previous exercise, this time using Jarrow and Rudd parametrization of the binomial tree.

#### Exercise 4.3

Consider an asset that trades at 100 and whose dynamics is represented by the CRR tree. The time horizon is _<sub>T</sub>_ \= 3 months and we set the step of the tree equal to one month. The annualized volatility of the UA returns is 30%. The risk-free rate is equal to 5%.

1.  Build the binomial tree with 3 months of horizon.
2.  Using this tree, compute the price of a forward contract with expiration in 3 months.
3.  Compare the previous result with the price obtained using the _cash and carry_ relation.

#### Exercise 4.4

Provide a graph showing the convergence of the value of the American put _<sub>P</sub>_ (0_<sub>,</sub>_1_<sub>/</sub>_4_<sub>,</sub>_95) with _<sub>S</sub>_ \= 100, _r_ \= 0_<sub>.</sub>_06, _<sub>y</sub>_ \= 0 and _<sub>σ</sub>_ \= 0_<sub>.</sub>_2 as a function of the first 100 steps of the Cox-Ross-Rubinstein. Answer the previous question, this time using the Broadie and Detemple (1996) correction.

#### Exercise 4.5

A CRR tree is used to model the dynamics of the UA price, which is currently 100. Return volatility is 30%. The risk-free rate is 5%. Consider the American call with 6-month maturity and 95 strike. The UA pays a dividend of _<sub>x</sub>_ in 3 months.

1.  Construct the binomial tree with two time steps, accounting for the UA price drop caused by the dividend.
2.  Compute the upper bound for _<sub>x</sub>_ below which the dividend is small enough to warrant no early exercise of the call.
3.  Check numerically that the result obtained above is close to _<sub>x < K</sub>_ 1 _<sub>− e</sub><sup>−r</sup>_<sup>(</sup>_<sup>T−td</sup>_<sup>)</sup> where _<sub>td</sub>_ denotes the dividend date. Explain why this inequality is a sufficient condition for no early exercise of the call.

#### Exercise 4.6

Consider the European put written on _<sub>S</sub>_ with time to maturity _<sub>T</sub>_ \= 1 year and strike price _<sub>K</sub>_ \= 110. The risk-free rate is 5%. Using a CRR tree with a single period, the possible values for _<sub>S</sub>_ are as follows: Today _S_ \= 100, upon maturity (in 1 year) _<sub>S</sub>_ \= 125 or _<sub>S</sub>_ \= 80.

1.  Determine the composition of the replication portfolio made of a position in _<sub>S</sub>_ and a position in the 1-year zero-coupon bond with nominal 100.
2.  Compute the initial value of the replication portfolio.
3.  Compute the delta of the put and compare it with the position in _<sub>S</sub>_ in the replication portfolio.
4.  Compute the value of the put and compare it with the initial value of the replication portfolio.
5.  Suppose now that there are some proportional transaction costs. Any purchase of the asset _<sub>S</sub>_ or of the zero-coupon bond costs in reality 101% of the theoretical price. Any sale of the asset _<sub>S</sub>_ or of the zero-coupon bond yields in reality 99% of the theoretical price. Revise your evaluation of the put.

#### Exercise 4.7

The XYZ stock is worth 44.75. The risk-free rate is 6.5%. The _variance_ of XYZ returns is 9.61%. There is no dividend. You wish to build a delta neutral portfolio with options on XYZ with strike 40 and maturity 71 (calendar) days.

. How many calls should you buy or sell if you own 100 XYZ stocks?

. How many stocks should you buy or sell if you are long 5 puts?

. How many puts should you buy or sell if you are long 1 call?

#### Exercise 4.8

You are holding a portfolio for speculative purposes. Your position is currently delta neutral and its gamma is +500. You are considering trading in a call with a 0.57 delta and a 2.5 gamma. What trades would you recommend if you still do not know in which direction the UA price will move and if you wish to minimize the future transaction costs?

#### Exercise 4.9

Using the BMS fundamental PDE, show that a delta neutral portfolio has a theta all the more negative since its vega is positive.

Hint: Use the analytical expressions of Greek parameters under the BMS model to relate the vega to the gamma.

Provide an interpretation in terms of dynamic management of the position.

#### Exercise 4.10

You wish to hedge the position of _<sub>np</sub>_ units in European puts with strike _<sub>K</sub>_ and maturity _<sub>T</sub>_. The replication portfolio consists of a position _<sub>nS</sub>_ in the UA, a position _<sub>nB</sub>_ on the money market and a position _<sub>nc</sub>_ in the European call with same characteristics. The UA pays no dividend. Determine _<sub>nS</sub>_, _<sub>nB</sub>_ and _<sub>nc</sub>_ as a function of _<sub>np</sub>_ when the replication strategy is delta-gamma neutral

#### Exercise 4.11

Consider the European call _<sub>g</sub>_ written on asset _<sub>S</sub>_ that does not pay any dividend. The call is issued by a financial institution that cannot deliver more than the quantity _<sub>x</sub>_ (_<sub>x <</sub>_ 1) of the UA. In other words, the call terminal payoff is as follows

_S_ (_T_) _− K_ if _xS_ (_T_) _≥ S_ (_T_) _− K ≥_ 0_, xS_ (_T_) if _S_ (_T_) _− K > xS_ (_T_)_,_

where _<sub>K</sub>_ and _<sub>T</sub>_ stand for the call strike and maturity.

1.  Show that the call _<sub>g</sub>_ can be written as the following linear combination of standard calls

_g_ \= _c_(_t,T,K_) _−_ (1 _− x_)_ct,T,_ 1_<sup>K</sup>− <sub>x</sub>._

1.  Use the preceding identity to explain why the value of _<sub>g</sub>_ is not strictly increasing with the volatility of returns on _<sub>S</sub>_. Provide a financial interpretation for this result.
2.  What can you say about the sign of the theta for _<sub>g</sub>_? What are the consequences for the American version of the call _<sub>g</sub>_ (same option with early exercise right)? Provide a financial interpretation for this result.

#### Exercise 4.12

You are holding one unit of a European option written on _<sub>S</sub>_ with strike _<sub>K</sub>_ and maturity _<sub>T</sub>_ and _<sub>x</sub>_ units of European options also written on _<sub>S</sub>_ with strike _<sub>K</sub><sup>∗</sup>_and maturity _<sub>T</sub><sup>∗</sup>_.

1.  Compute the BMS gamma of your portfolio.
2.  Compute the BMS vega of your portfolio.
3.  What condition(s) must be verified by your options characteristics for your portfolio to be gammavega neutral?

**4.6 Solutions**

#### Solution 4.1

Using the CRR tree, we get _c_(0_<sub>,</sub>_1_<sub>/</sub>_2_<sub>,</sub>_120) = _<sub>C</sub>_ (0_<sub>,</sub>_1_<sub>/</sub>_2_<sub>,</sub>_120) = 12_<sub>.</sub>_763, _<sub>p</sub>_(0_<sub>,</sub>_1_<sub>/</sub>_2_<sub>,</sub>_120) = 6_<sub>.</sub>_058 and _<sub>P</sub>_ (0_<sub>,</sub>_1_<sub>/</sub>_2_<sub>,</sub>_120) = 6_<sub>.</sub>_385\. The deltas of the American options are

∆_<sub>c</sub>_ \= 0_<sub>.</sub>_6414_<sub>,</sub>_ ∆_<sub>p</sub>_ \= _−_0_<sub>.</sub>_3875_<sub>.</sub>_

When gamma is computed as the first order partial derivative of ∆ with respect to _<sub>S</sub>_, we get Γ_<sub>c</sub>_ \= 0_<sub>.</sub>_0193_<sub>,</sub>_ Γ_<sub>p</sub>_ \= 0_<sub>.</sub>_0221.

#### Solution 4.2

Using the Jarrow-Rudd tree, we get _c_(0_<sub>,</sub>_1_<sub>/</sub>_2_<sub>,</sub>_120) = _<sub>C</sub>_ (0_<sub>,</sub>_1_<sub>/</sub>_2_<sub>,</sub>_120) = 12_<sub>.</sub>_625, _<sub>p</sub>_(0_<sub>,</sub>_1_<sub>/</sub>_2_<sub>,</sub>_120) = 5_<sub>.</sub>_923 and _<sub>P</sub>_ (0_<sub>,</sub>_1_<sub>/</sub>_2_<sub>,</sub>_120) = 6_<sub>.</sub>_310\. The deltas of the American options are

∆_<sub>c</sub>_ \= 0_<sub>.</sub>_6658_<sub>,</sub>_ ∆_<sub>p</sub>_ \= _−_0_<sub>.</sub>_3737_<sub>.</sub>_

When gamma is computed as the first order partial derivative of ∆ with respect to _<sub>S</sub>_, we get Γ_<sub>c</sub>_ \= 0_<sub>.</sub>_195_<sub>,</sub>_ Γ_<sub>p</sub>_ \= 0_<sub>.</sub>_223.

#### Solution 4.3

(a) The values of the UA are

##### _t_ ~~\= 0~~ _<sub>t</sub>_ ~~\= 1~~ _<sub>t</sub>_ ~~\= 2~~ _<sub>t</sub>_ ~~\= 3~~

_S_ (_<sub>t</sub>_) 129.668

118.911 109.046

109.046 100 91.704

100 91.704 84.097 77.12

1.  Upon maturity, the UA forward price is equal to the UA spot price. Before maturity, forward prices are obtained with backward induction by applying their martingale property. Which yields

|     |     |     |     |
| --- | --- | --- | --- |
| _t_ \= 0 | _t_ \= 1 | _t_ \= 2 | _t_ \= 3 |
| _f_ (_t,T_) |     |     | 129.668 |
|     |     | 119.407 | 109.046 |
|     | 109.959 | 100.418 | 91.704 |
| 101.258 | 92.472 | 84.448 | 77.12 |

Hence _<sub>f</sub>_ (0_<sub>,</sub>_3_<sub>/</sub>_12) = 101_<sub>.</sub>_258_<sub>.</sub>_

1.  From the _cash and carry_ relation, we readily obtain

_f_ (0_,_3_/_12) = 100_e_<sup>0</sup>_<sup>.</sup>_<sup>05</sup><sub>12</sub><sup>3</sup> \= 101_._258_._

#### Solution 4.4

Using the CRR tree, we obtain the following graph

20

40

60

80

100

n

1.48

1.52

1.54

1.56

Put

Figure 4.8: CRR values.

which illustrates the irregular convergence. Applying the Broadie and Detemple (1996) correction, which consists in initializing the pricing algorithm at the former to last node with the BMS, one step to maturity option prices, we obtain the following graph

20

40

60

80

100

n

1.52

1.5225

1.525

1.5275

1.53

1.5325

1.535

Put

Figure 4.9: CRR+BD96 values.

The convergence appears to be much faster and much smoother.

#### Solution 4.5

1.  Using

_u_ \= exp0_._3<sup>q</sup>3_/_12 \= 1_._1618_,_

we obtain the following CRR tree

|     |     |     |
| --- | --- | --- |
| Today | 3 months | 6 months |
| 100 | 116_<sub>.</sub>_18 |     |
|     | 116_._18 _− x_ | 134_<sub>.</sub>_98 _−_ 1_<sub>.</sub>_1618_<sub>x</sub>_ 100 _−_ 0_<sub>.</sub>_8607_<sub>x</sub>_ |

86_<sub>.</sub>_07

86_._07 _− x_ 100 _−_ 1_._1618_x_

74_<sub>.</sub>_09 _−_ 0_<sub>.</sub>_8607_<sub>x</sub>_

1.  The probability of an upward move is

exp0_._05 _×_ 123 _−_ 1_._16181 _π_ \= 1_._1618 _−_ 1_._1618<sub>1</sub> \= 0_._50436_._

Therefore a sufficient condition for no exercise in 3 months is

116_<sub>.</sub>_18 _−_ 95 _<sub><</sub>_ exp_−_0_<sub>.</sub>_0512<sup>3</sup> \[0_<sub>.</sub>_50436(134_<sub>.</sub>_98 _−_ 1_<sub>.</sub>_1618_<sub>x</sub> −_ 95)

+(1 _−_ 0_<sub>.</sub>_50436)(100 _−_ 0_<sub>.</sub>_8607_<sub>x</sub> −_ 95)\]_<sub>,</sub>_

where it has been implicitly assumed that the call will be exercised at maturity in all states of the world. Which yields

_x <_ 1_._181_._ (c) We check that

_K_ (1 _−_ exp(_−<sub>r</sub>_(_T − <sub>td</sub>_))) = 951 _−_ exp_−_0_._0512<sup>3</sup> \= 1_._180_._

Upon early exercise, we get _<sub>Std</sub> − <sub>K</sub>_ (dividend capture). If we decide not to exercise, we get at least the value of the European call written on _<sub>Std</sub> −<sub>x</sub>_ with time to maturity _<sub>T −td</sub>_. A no-arbitrage lower bound for that European call is

_S<sub>t</sub>d − x − Ke−r_(_T−t<sup>d</sup>_)_._

Thus, a sufficient condition for no early exercise is

_Std − K < Std − x − Ke−r_(_T−td_)_,_

or, equivalently,

_x < K_ 1 _− e−r_(_T−t<sub>d</sub>_)_._

#### Solution 4.6

1.  Let _<sub>a</sub>_ denote the position in asset _<sub>S</sub>_ and _<sub>b</sub>_ denote the position in the zero-coupon bond. The replication portfolio must be such that

0 = _<sub>a</sub> ×_ 125 + _<sub>b</sub> ×_ 100_<sub>,</sub>_ 30 = _<sub>a</sub> ×_ 80 + _<sub>b</sub> ×_ 100_<sub>.</sub>_

Which yields

_a_ \= _−__, b_ \= _._

1.  The initial value of the replication portfolio is

Π = _−_ _×_ 100 +  _×_ 100 _× <sub>e</sub><sup>−</sup>_<sup>0</sup>_<sup>.</sup>_<sup>05</sup> \= 12_._602_._

1.  The put delta is given by

∆_<sub>p</sub>_ \=  = _−__,_

which is the position in _<sub>S</sub>_ indeed. (d) The value of the put is

_p_ \= 30 _× e−_0_._05 125 _− e_0_._05 = 12_._602_,_

100 _−_ 100

which corresponds to the value of the replication portfolio. (e) With transaction costs, the value of the put is now given by

_p_ \= _−_ _×_ 99 +  _×_ 101 _× <sub>e</sub><sup>−</sup>_<sup>0</sup>_<sup>.</sup>_<sup>05</sup> \= 14_._062_._

**Solution 4.7**

Sell 119 calls. Buy 0.816 units of UA. Buy 5.13 puts.

**Solution 4.8**

Sell 200 calls and buy 114 units of UA.

#### Solution 4.9

The PDE for portfolio _<sub>W</sub>_ becomes

_σ θ<sub>W</sub>_ \= _rW −_ 2_T ϑ<sub>W</sub> ._

Implication: A speculative strategy that is betting on an increase in volatility (highly positive vega) must be right quickly because it is losing money as time goes by (highly negative theta).

#### Solution 4.10

The self-financing, delta neutrality and gamma neutrality conditions imply that

_n<sub>p</sub>p_ \+ _n<sub>c</sub>c_ \+ _n<sub>S</sub>S_ \+ _n<sub>B</sub>B_ \= 0_, n<sub>p</sub>_∆_<sub>p</sub>_ \+ _n<sub>c</sub>_∆_<sub>c</sub>_ \+ _n<sub>S</sub>_ \= 0_, n<sub>p</sub>_Γ_<sub>p</sub>_ \+ _n<sub>c</sub>_Γ_<sub>c</sub>_ \= 0_._ From put-call parity we get Γ_<sub>p</sub>_ \= Γ_<sub>c</sub>_ and ∆_<sub>c −</sub>_ ∆_<sub>p</sub>_ \= 1. Which yields

|     |     |     |
| --- | --- | --- |
| _n<sub>c</sub>_ | \=  | _−n<sub>p</sub>,_ |
| _n<sub>S</sub>_ | \=  | _n<sub>p</sub>,_ |
| _nB_ | \=  | _−n<sub>p</sub>K._ |

#### Solution 4.11

1.  The table below establishes the net position of being long one unit of _<sub>c</sub>_(_<sub>t,T,K</sub>_) and short (1 _<sub>− x</sub>_) units of _ct,T,_ <sub>1</sub>_<sup>K</sup><sub>−x</sub>_.

_S_

(

_T_

)

_≤_

_K_

_K < S_

(

_T_

)

_≤_

_K_

1

_−_

_x_

_K_

1

_−_

_x_

_<_

_S_

(

_T_

)

_c_

(

_t,T,K_

0

)

_S_

(

_T_

)

_−_

_S_

_K_

(

_T_

)

_−_

_K_

(1

_−_

_x_

)

_c_

_t,T,_

_K_

1

_−_

_x_

(1

0

0

_−_

_x_

)

_S_

(

_T_

)

_−_

_K_

1

_−_

_x_

0

Net position

_S_

(

_T_

)

_−_

_K_

_xS_

(

_T_

)

We see the net position replicates the call _<sub>g</sub>_.

1.  The payoff of _<sub>g</sub>_ is convex around _<sub>K</sub>_ (slope increases from 0 to +1), and then it is concave around _K/_(1 _<sub>− x</sub>_) (slope decreases from +1 to +_<sub>x</sub>_). Hence for low values of _<sub>S</sub>_ the value of _<sub>g</sub>_ increases with volatility. But for _<sub>S > K/</sub>_(1 _− <sub>x</sub>_) it decreases with volatility.

Interpretation: if _<sub>S</sub>_ gets very volatile, there are greater chances that the payoff of _<sub>g</sub>_ be capped by _xS_ (_<sub>T</sub>_) because of the delivery constraint.

1.  The theta of a European call is negative. Hence the sign of the theta of _<sub>g</sub>_ is undetermined. Thus, there will be cases where the early exercise of _<sub>g</sub>_ is valuable. That is, in contrast to standard European calls written on a non-dividend paying UA, _<sub>G ≥ g</sub>_ where _<sub>G</sub>_ is the American version of _<sub>g</sub>_.

Interpretation: early exercise can be valuable to avoid the delivery constraint to bind in the future. By exercising now (and paying _<sub>K</sub>_), the option holder is guaranteed to benefit from the full upside of _S_.

#### Solution 4.12

1.  Under the BMS assumptions, the gamma of portfolio Π is

Γ<sub>Π</sub> \= _<sup>√</sup>_ \+ _x √ ._

_Sσ T Sσ T<sup>∗</sup>_

1.  The vega of that portfolio is

_._

1.  Setting Γ<sub>Π</sub> \= _<sub>ϑ</sub>_<sub>Π</sub> \= 0, we obtain the following system



_,_

 _S__,_

or, alternatively,

q_T∗_

 _x T ,_

<sub></sub> _x_ _._

That system admits a solution only if _<sub>T</sub>_ \= _<sub>T</sub><sup>∗</sup>_. The two options must have the same maturity.

**Chapter 5**

**Exotic options**

Exotic options (sometimes referred to as second generation options) are derivatives offering a non-standard payoff. Many of them were initially engineered on the foreign exchange market in the 1980s and the 1990s. Their introduction allowed for a wider array of hedging or speculative solutions to investors. They are more thinly traded than vanilla options and therefore do not enjoy the same level of liquidity. Depending on the complexity of their payoff, exotic options can be harder to evaluate and to replicate. In this chapter, we focus on the analytical solutions that are available in the BMS framework.

**5.1 Barrier-type options**

#### 5.1.1 Vanilla barrier options

The standard barrier calls and puts yield the same terminal payoffs as their European counterparts. The only difference is that this payoff is subject to the first hitting time of the UA price with respect to a contractual level _<sub>H</sub>_ (the barrier). A first distinction is whether the current UA price is below the barrier (_<sub>S < H</sub>_), in which case the barrier option is of the ”up” type, or the current UA price is above the barrier (_<sub>S > H</sub>_), in which case the barrier option is of the ”down” type. Next, the contract must specify what happens the first time the barrier is hit. Either the right to the payoff is activated (the barrier option is of the ”in” type), or it disappears (the barrier option is of the ”out” type).

When these two elements are combined, there are theoretically eight types of barrier options, namely up&in, up&out, down&in and down&out calls and puts. In practice, barrier options are the most attractive to investors when they actually reduce the cost of hedging. That is, when the hedge is activated only when needed or when the hedge is deactivated when not needed. Consequently, the following four types of barrier options are the most valuable:

Hedge for Hedge for

a short position a long position up&in call up&out put

down&out call down&in put

Typically the up&in call and down&in put are activated when they are ITM, while the down&out call and the up&out put are deactivated when they are OTM.

127

All else equal, barrier options are cheaper than vanilla options with same characteristics. This is because they promise the same payoff but subject to an additional condition. Not surprisingly, a cheaper hedge implies a less perfect hedge. As far as ”in” options are concerned, there is the risk that the hedge never appears because the barrier was not activated during the life of the contract. That risk can be mitigated by selecting the barrier level not too far away from the current UA price. More serious is the risk specific to ”out” options that the deactivating barrier is hit before maturity (and the hedge is lost) and then the UA price upon maturity moves to an unfavorable direction. For example, an investor hedging a short position might want to buy a down&out call (instead of a vanilla call). If the UA price goes down enough (deactivating the option), then the position is vulnerable if the UA price goes up afterwards. One solution to mitigate this risk is to make a new hedging decision when the barrier option disappears.

Barrier options are usually European-style. It is, however, possible to add an early exercise right in the contract specification and design an American barrier option.

Pricing formulae for European barrier options are available in closed-form within the BMS framework. The formula for the down&out call was initially derived by Merton (1973). Reiner and Rubinstein (1991) provide a comprehensive set of valuation results. Solutions are obtained from the Brownian motion _reflection principle_. In the next subsection we present a detailed proof for the value of the down&in call by applying this principle. All other barrier options can be valued by adapting this proof or by using simple parity relations (see below). Define

_a_ \= _SH_(0)2(_rσ−_2_y_)_−_1 _, b_ \= _SH_(0)+1 _,_

and

 (0) _<sub>−</sub>_ _√_

_z_<sub>1</sub> \=_z_<sub>2</sub> \= _z_<sub>1</sub> _− σ T, z_<sub>3</sub> \=_z_<sub>4</sub> \= _z_<sub>3</sub> _− σ√T,_

_√_

_z_<sub>5</sub> \=_z_<sub>6</sub> \= _z_<sub>5</sub> _− σ T,_

_√_

_z_<sub>7</sub> \=_, z_<sub>8</sub> \= _z_<sub>7</sub> _− σ T._

_σ T_

The premium for the up&out call when _<sub>H > K</sub>_ is

_c<sub>u</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_) = _S_(0)_e<sup>−yT</sup>_ \[Φ(_z_<sub>1</sub>) _−_ Φ(_z_<sub>3</sub>) _− b_(Φ(_z_<sub>6</sub>) _−_ Φ(_z_<sub>8</sub>))\] _−Ke<sup>−rT</sup>_ \[Φ(_z_<sub>2</sub>) _−_ Φ(_z_<sub>4</sub>) _− a_(Φ(_z_<sub>5</sub>) _−_ Φ(_z_<sub>7</sub>))\]_,_

otherwise _<sub>cu</sub>_<sub>&</sub>_<sub>o</sub>_(0_<sub>,T,K,H</sub>_) = 0. Besides, a parity relation (for barrier options with same characteristics) yields

_c<sub>u</sub>_<sub>&</sub>_<sub>i</sub>_(0_,T,K,H_) = _c_(0_,T,K_) _− c<sub>u</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_)_._

The premium for the down&out call when _<sub>H > K</sub>_ is

_c<sub>d</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_) = _S_(0)_e<sup>−yT</sup>_ \[Φ(_z_<sub>3</sub>) _− b_(1 _−_ Φ(_z_<sub>6</sub>))\]

_−Ke<sup>−rT</sup>_ \[Φ(_z_<sub>4</sub>) _− a_(1 _−_ Φ(_z_<sub>5</sub>))\]_,_

and when _<sub>H</sub> ≤ <sub>K</sub>_ it is

_c<sub>d</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_) = _S_(0)_e<sup>−yT</sup>_ \[Φ(_z_<sub>1</sub>) _− b_(1 _−_ Φ(_z_<sub>8</sub>))\]

_−Ke<sup>−rT</sup>_ \[Φ(_z_<sub>2</sub>) _− a_(1 _−_ Φ(_z_<sub>7</sub>))\]_._

Moreover,

_c<sub>d</sub>_<sub>&</sub>_<sub>i</sub>_(0_,T,K,H_) = _c_(0_,T,K_) _− c<sub>d</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_)_._

Regarding the up&out put with _<sub>H > K</sub>_, we obtain

_p<sub>u</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_) = _Ke<sup>−rT</sup>_ \[1 _−_ Φ(_z_<sub>2</sub>) _− a_Φ(_z_<sub>7</sub>)\]

|     |     |     |
| --- | --- | --- |
| and with _H ≤ K_ |     | _−S_(0)_e<sup>−yT</sup>_ \[1 _−_ Φ(_z_<sub>1</sub>) _− b_Φ(_z_<sub>8</sub>)\]_,_ |
| _p<sub>u</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_) | \=  | _Ke<sup>−rT</sup>_ \[1 _−_ Φ(_z_<sub>2</sub>) _− a_(Φ(_z_<sub>7</sub>) _−_ Φ(_z_<sub>5</sub>))\] _−S_(0)_e<sup>−yT</sup>_ \[1 _−_ Φ(_z_<sub>1</sub>) _− b_Φ(_z_<sub>8</sub>)\]_._ |

In addition,

_p<sub>u</sub>_<sub>&</sub>_<sub>i</sub>_(0_,T,K,H_) = _p_(0_,T,K_) _− p<sub>u</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_)_._

Finally, as far as the down&out put is concerned, when _<sub>H ≤ K</sub>_

_p<sub>d</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_) = _Ke<sup>−rT</sup>_ \[Φ(_z_<sub>4</sub>) _−_ Φ(_z_<sub>2</sub>) _− a_(Φ(_z_<sub>7</sub>) _−_ Φ(_z_<sub>5</sub>))\]

_−S_(0)_e<sup>−yT</sup>_ \[Φ(_z_<sub>3</sub>) _−_ Φ(_z_<sub>1</sub>) _− b_(Φ(_z_<sub>8</sub>) _−_ Φ(_z_<sub>6</sub>))\]_,_

otherwise _<sub>pd</sub>_<sub>&</sub>_<sub>o</sub>_(0_<sub>,T,K,H</sub>_) = 0. A parity relation yields

_p<sub>d</sub>_<sub>&</sub>_<sub>i</sub>_(0_,T,K,H_) = _p_(0_,T,K_) _− p<sub>d</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H_)_._

All these formulae assume the continuous monitoring of the barrier. In practice, barrier option contracts specify the observation frequency of the activating or deactivating threshold (a standard case is the daily monitoring of the end-of-day quote). Broadie et al. (1997) show how to adjust the BMS pricing of vanilla barrier options when the barrier is monitored at discrete dates. For calls of the ”out” type or for puts of the ”in” type, they prove (and confirm it by means of simulations) that a good approximation is given by

_O<sub>d</sub>_ (0_,T,K,H_)_,T,K,H_ _t,_

where subscript _<sub>d</sub>_ (_<sub>c</sub>_) refers to a discretely (continuously) monitored barrier, ∆_<sub>t</sub>_ is the time interval between two observations, _<sub>σ</sub>_ is the UA return volatility and _<sub>±</sub>_ takes the positive (negative) sign when _<sub>H > S</sub>_(0) (_H < S_(0)).

#### 5.1.2 The reflection principle

Without any loss in generality, we are considering the down&in call with _<sub>H ≤ K</sub>_. The premium for the down&out call is retrieved from a parity relation. In the AoA, the premium for the down&in call is the solution to

_cd_&_i_(0_,T,K,H_) = _e−rT_ EQh(_S_(_T_) _− K_)+ 1_τ<T_ i_,_

where _<sub>τ</sub>_ denotes the (random) first time when the UA price hits the level _<sub>H</sub>_ (thereby activating the call). Formally,

_τ_ \= inf _{t ≥_ 0 : _S_(_t_) = _H},_

or, alternatively,

_._

To simplify notations, we set

_<sub>m</sub>_ \= _r − y − σ_<sup>2</sup>_/_2_<sub>,</sub>_

_b_ \= _S_(0)

_σ_

1

_σ_

ln

_H_

_,_

|     |     |
| --- | --- |
| which yields | _W_<sub>f</sub>_<sub>t</sub>_ \= _W<sub>t</sub>_ \+ _mt,_ |

_τ_ \= inf <sup>n</sup>_t ≥_ 0 : _W_<sub>f</sub>_<sub>t</sub>_ \= _b_<sup>o</sup>_._

Consider the following change of probability measure

_dd_QQ2 = exp _m_22 _t − mW_f_t_! = exp _−m_22 _t − mWt_!_._

From Girsanov theorem, we know that _<sub>W</sub>_<sub>f</sub>_<sub>t</sub>_ is a Brownian motion under Q2. We apply this change of probability measure to compute the premium as a Q2-expectation

EQh(_S_(_T_) _− K_)+ 1_τ<T_ i

" + _m_2 #

\= EQ<sup>2</sup> _S_(0)_eσW_e_<sup>T</sup> − K e−_ <sub>2</sub> _T_+_mW_e_<sup>T</sup>_ 1_<sub>τ<T</sub>_

\= EQ2 _S_(0)_eσW_e_T − Ke__mW_e_T_ 1_τ<T_ 1_WT>_ ln _._

e 

Define

_φ_(_x_) = EQ2 _exW_e_T_ 1_τ<T_ 1_WT>σ_1 ln _K_(0)

e _S_

\= Z _∞ W_f_T ∈ dw,τ < T,_

<sup>1</sup> ln

then the down&in call premium can be written as

_cd_&_i_(0_,T,K,H_) = _S_(0)_e−rT e−m_22 _T φ_(_m_ \+ _σ_) _− Ke−rT e−m_22 _T φ_(_m_)_._

To determine the function _<sub>φ</sub>_(_<sub>.</sub>_), we are resorting to the reflection principle of the Brownian motion, which states the following

Proba(_W<sub>T</sub> ∈ dw,τ < T_) = Proba(_W<sub>T</sub> ∈_ (2_b − dw_))_._

To understand this equality, consider a Brownian motion _<sub>Wt</sub>_ starting above level _<sub>b</sub>_. Our goal is to count all the paths such that _<sub>Wt</sub>_ reaches _<sub>b</sub>_ before _<sub>T</sub>_ and ends up its course at some level _<sub>w > b</sub>_. Figure 5.1 illustrates the reflection principle.

Figure 5.1: The reflection principle. Once the barrier _<sub>b</sub>_ is hit, consider the mirrored path around _<sub>b</sub>_ (shown in dashed line). Since the initial path ends up at level _<sub>w</sub>_, then by symmetry around _<sub>b</sub>_ the mirrored path ends up at level 2_<sub>b − w</sub>_. Given the properties of the Brownian motion (in particular the fact that its conditional distribution is symmetric around its current value), the mirrored path (in dashed line) is equally likely than the initial path (in solid line). Hence the reflection principle states that it is equivalent to count all the paths illustrated by the solid line or to count all the paths illustrated by the solid line until _<sub>b</sub>_ and then by the dashed line.

But it turns out that counting the mirrored paths is much easier since the first hitting time condition no longer matters. Indeed, if _<sub>Wt</sub>_ starts above _<sub>b</sub>_ and end ups at level 2_<sub>b−w < b</sub>_, then owing to the continuous path of the Brownian motion, there must exist a time before _<sub>T</sub>_ when _<sub>Wt</sub>_ has hit level _<sub>b</sub>_. Applying the reflection principle, we thus obtain

_φ_(_x_) = _√_ 1 Z _∞ exwe−_21_T_ (_w−_2_b_)2_dw._

2_πT_ <sub>ln</sub>

The change of variable _<sub>y</sub>_ \= _<sub>w</sub> −_ (2_<sub>b</sub>_ \+ _<sub>Tx</sub>_) yields

_φ_(_x_) = exp 2_Tx_ \+ 2_bx_ Φ _~~√~~<sub>T</sub>_ \+ _√Tx_ \+ _<sub>σ</sub>~~√~~<sub>T</sub>_ ln _S<sub>K</sub>_<sup>(0)</sup>_,_

1

2

2

_b_

1

or, given the definition of _<sub>b</sub>_

|     |     |     |
| --- | --- | --- |
| 2<br><br>Simple algebra leads to | _S_(0) | _σ T KS_(0) |

_Tx_2 ! _H_ 1 ln _H_2 + _√Tx_!_. <sup>φ</sup>_(_<sup>x</sup>_) = expΦ _√_

2

_x_

_σ_

|     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- |
| _c<sub>d</sub>_<sub>&</sub>_<sub>i</sub>_(0_,T,K,H_) | \=  | _S_(0)_e_ | _S_(0) | Φ<sub></sub> | _√ σ T_ |    |

  _<sup>−yT H</sup> T_

  

_−Ke−rT_ _H_ Φ _√ T_ _._

_S_(0) _σ T_

#### 5.1.3 Parisian options

With vanilla barrier contracts, options are activated or deactivated by the mere first hit of the UA price to the threshold. In volatile times, such hit might be an accident and may not represent the real trend of the UA price. Parisian options have been designed to address this problem. Consider without any loss in generality knock-out options. A down&out Parisian call will not be deactivated on the simple first hitting time criterion. Rather, it will take a certain number of _consecutive_ observations below the threshold for the option to disappear. The length of the consecutive time period spent underneath the barrier is called the window. Figure 5.2 shows how the down&out Parisian call is deactivated.

Figure 5.2: Parisian down & out with window _<sub>D</sub>_.

In the BMS framework, Chesney et al. (1997) show that the value of the down&in Parisian call with maturity _<sub>T</sub>_, strike _<sub>K</sub>_, barrier _<sub>H</sub>_ and window _<sub>D</sub>_ is given by

Z _∞_

_c<sup>par</sup><sub>d</sub>_<sub>&</sub>_<sub>i</sub>_(0_,T,K,H,D_<sup>) =</sup> 1 _K e<sup>mu</sup>_ (_S_(0)_e<sup>σu</sup> − K_)_h_(_T,u_)_du,_

_σ_ <sup>ln</sup> _S_(0)

with _<sub>m</sub>_ \= _<sub>σ</sub>_<sup>1</sup> _<sub>r</sub> − <sub>y</sub> − <sup>σ</sup>_<sub>2</sub><sup>2</sup> . To perform the numerical integration, the function _<sub>h</sub>_(_<sub>x,u</sub>_) must be computed by inverting its Laplace transform, which is

_√_

_h_<sub>b</sub> (_x,u_) = <sup>Z</sup> _∞ z_ exp _−_2_<sup>z</sup><sub>D</sub>_<sup>2</sup> _− |b − z − u|√_~~2~~_x_<sup>!</sup>_dz,_

_e_

_b_

2

_x_

_√_

2

_x_

Ψ

_√_

2

_<sub>D xD</sub>_ <sub>0</sub>

with _<sub>b</sub>_ \=  ln _<sub>S</sub><sup>H</sup>_<sub>(0)</sub> and Ψ(_<sub>x</sub>_). In the case where _<sub>K > H</sub>_, this Laplace transform simplifies into

_√_

Ψ

_−_

_√_

2

_xD_

_√_

_xD_

_e_

(2

_b_

_−_

_y_

)

2

_x_

_√_

2

_h_<sub>b</sub> (_x,y_) =_._

Ψ 2 _x_ Similar to vanilla barrier options, we have the following parity relation

_c<sup>par</sup><sub>d</sub>_<sub>&</sub>_<sub>o</sub>_(0_,T,K,H,D_) = _c_(0_,T,K_) _− c<sup>par</sup><sub>d</sub>_<sub>&</sub>_<sub>i</sub>_ (0_,T,K,H,D_)_._

In addition, Chesney et al. (1997) establish the following put-call parity for Parisian options

_par_ (0_,T,K,H,D_) = _S_(0)_Kcparu_&_o_ 0_,T, K_1 _, H_1 _,DS_ \= _S_(0)1 _._

_pd_&_o_

Haber et al. (1999) show how to apply the finite difference numerical method (see next chapter) to evaluate Parisian options. Fusai and Tagliani (2001) examine the impact of the observation frequency on the value of Parisian options. More generally, Hugonnier (1999) presents a method to value derivatives whose payoff is defined according to the _excursion_ of the UA price, that is, the behavior of the Brownian motion under a given threshold. That approach allows in particular to deal with ”Parasian” options that are similar contracts except that the activating or deactivating criterion is not based on the consecutive time but on the _cumulative time_ spent above or below the barrier. In other words, the clock counting the number of observations is not reset to zero every time the UA price moves out of the excursion zone (see Moraux, 2019, for a deeper study of that derivative).

Anderluh and van der Weide (2004) provide an approximation for the value of the up&in Parisian call using a vanilla up&in call

_cparu_&_i_ (0_,T,K,H,D_) _≃ cu_&_i_ 0_,T,K,H_ _D_r_π_2_,_

where _<sub>m</sub>_ keeps the same definition.

It is difficult to obtain a reliable adjustment for Parisian options with discrete monitoring of the barrier (similar to Broadie et al., 1997, for vanilla barrier options). Bernard and Boyle (2011) note that the two contract modifications: (i) from a continuously observed barrier to a discretely observed barrier, and (ii) from a vanilla barrier option to a Parisian barrier option – generate opposite biases. Let us take the example of the up&in call. For a given threshold level, the discrete monitoring of the barrier reduces the value of the call (there are fewer chances of activating the contract). However, the discretely monitored Parisian call is more valuable than its continuously monitored counterpart because, for a sufficiently long window, it will be easier to activate the Parisian option if the required consecutive prices are observed at certain discrete dates only.

#### 5.1.4 Double barrier options

An extension to vanilla barrier options consists in defining two barriers in the contract, one above the current UA price level (_<sub>Hu</sub>_) and the other below (_<sub>Hd</sub>_). For instance, a double knock-in call is a call that will be activated the first time the UA price reaches the threshold _<sub>Hu</sub>_ or the threshold _<sub>Hd</sub>_, whichever comes sooner.

A boost option is a type of double knock-out option. To determine its payoff, one first counts the number of days that the UA price remained inside the band \[_<sub>Hd</sub>,H<sub>u</sub>_\] until maturity _<sub>T</sub>_. Then this number of days is multiplied by the face value of the contract to get a payoff in dollars. By design boost options have a rather uncommon feature: Their vega is usually negative.

**5.2 Average-type options**

#### 5.2.1 Contract characteristics

Exotic options whose payoff is computed on some average of UA prices are often referred to Asian options. Since averages are by construction less volatile, these options are typically cheaper than their vanilla counterparts.

Asian options can have a fixed strike or a floating strike. In the first case, the terminal payoff of the call is

max(_M_(_T_) _− K,_0)_,_

where _<sub>M</sub>_(_<sub>T</sub>_) denotes some average of UA prices. These options are convenient for hedging purposes. Indeed, for an agent exposed to repeated positions (e.g., a corporate Treasurer that regularly pays a supplier in foreign currency, say every month), hedging the cumulated position with an Asian option stands as a cheaper alternative to hedging every single position with a collection of vanilla options. In this strategy, the strike _<sub>K</sub>_ keeps the same interpretation: It corresponds to the worst conditions guaranteed by the hedge.

With a floating strike, the terminal payoff of the call is

max(_S_(_T_) _− M_(_T_)_,_0)_,_

i.e., the average stands as the strike. This type of Asian options is less suited for a hedging strategy (since there is no fixed amount in the payoff). They are more appealing for speculative purposes.

The average _<sub>M</sub>_(_<sub>T</sub>_) can be computed over the entire duration of the contract, or over any pre-specified subperiod. As with barrier options, it is subject to an observation frequency. There are some analytical formulae available for continuous Asian options but these are only approximations to real-life, discretely monitored contracts.

Finally, most Asian options rely on the arithmetic average. These options admit no closed-form solutions in the BMS framework. The reason is that the distribution of the sum of log-normal variables is unknown in general. Of particular interest is the case where the Asian option relies on the geometric average. Since the geometric average of log-normal variables is log-normally distributed as well, Asian options with geometric averaging can be valued analytically in the BMS framework. Their valuation only requires a slight drift and volatility adjustment in the standard BMS valuation formulae for European options (see the next subsection).

The following tables summarizes the different specifications for the average _<sub>M</sub>_(_<sub>T</sub>_)

|     |     |     |
| --- | --- | --- |
| Average | Monitoring Continuous | Discrete |
| Arithmetic | <sup>1 R</sup> _<sup>T</sup> S_(_t_)_dt_<br><br>_T_ 0 | 1 P_N S_(_t_) _N t_\=1 |
| Geometric | exp <sup>1 R</sup> _<sup>T</sup>_ ln_S_(_t_)_dt_<br><br>_T_ 0 | _N_ !1_/N_ <sup>Y</sup> ( )<br><br>_S t_<br><br>_t_\=1 |

As with barrier options, Asian options are usually European-style. It is, however, possible to add an early exercise right in the contract specification and design an American Asian option.

#### 5.2.2 Asian option with geometric averaging

In the BMS framework, where the UA returns are normally distributed with risk-neutral drift _<sub>r − y</sub>_ and volatility _<sub>σ</sub>_, the returns on the continuous, geometric average are also normally distributed (see Kemna and Vorst, 1990, Conze and Viswanathan, 1991a, or Angus, 1999). This type of average therefore follows a GBM but with modified drift and volatility, namely

!

Drift (_<sub>M,</sub>_

Volatility (_<sub>M</sub>__<sub>.</sub>_

Hence fixed strike Asian options can be evaluated using the corresponding BMS formulae for European options using input convenience yield _<sub>y</sub><sup>∗</sup>_ such that

! _y,_

and input volatility

_._

Note that, as expected, the average is less volatile than the underlying price. When the average i_<sub>√</sub>_s geometric and the underlying price is log-normally distributed, the volatility reduction is by a factor of 3. Turnbull and Wakeman (1991) and Ritchken et al. (1993) extend this result when the geometric average is monitored in discrete time.

The proof for these drift and volatility adjustments is as follows. The average is given by

_M_(_T_) = exp <sup>1 Z</sup> _<sup>T</sup>_ ln(_S_(_t_))_dt_<sup>!</sup>_<sub>.</sub>_

_T_ <sub>0</sub>

Expanding that expression, we get

_M_(_T_) = exp _T_1 Z _T_ ln _S_(0)exp" _r − y − σ_22 !_t_ \+ _σWt_#!_dt_!

0

" _σ_2 ! _T_ \# _σ_ <sub>Z</sub> _T_ !

\= _<sup>S</sup>_(0)exp _r − y −_ 2 2 exp _<sub>T</sub>_ 0 _W<sub>t</sub>dt ._

Let us focus on <sup>R</sup><sub>0</sub>_<sup>T</sup> <sub>Wtdt</sub>_. Integrating by parts yields

Z _T_ Z _T_

_W<sub>t</sub>dt_ \= _TW<sub>T</sub> − tdW<sub>t</sub>._

0 0

Hence <sup>R</sup><sub>0</sub>_<sup>T</sup> <sub>Wtdt</sub>_ appears as a Brownian motion less a Wiener integral. As such, it is the linear combination of centered, Gaussian variables, thus it is a centered, Gaussian variable, too. Its variance is

_T_ !  Z _T_ !2 Z _T_ 

Z

V_ar W<sub>t</sub>dt_ \= E<sub></sub>(_TW<sub>T</sub>_ )<sup>2</sup> \+ _tdW<sub>t</sub> −_ 2_TW<sub>T</sub> tdW<sub>t</sub>_<sub></sub>

0 0 0

\= _T_3 + _T_33 _−_ 2_T_ Z0_T tdt_ \= _T_33 _._

Consequently, the average can be written as

" _<sup>σ</sup>_2 ! _T_ \# _σ √_ _M_(_T_) = _S_(0)exp _r − y −_ 2 2 exp _~~√~~_~~3~~ _Tε ._

Let Σ = _<sub>σ/</sub><sup>√</sup>_~~3~~, we obtain after some algebra

" _M_(_T_) = _S_(0)exp _r._

We recognize the solution of the GBM with volatility Σ and drift .

#### 5.2.3 Asian option with arithmetic averaging

As we mentioned, Asian options with arithmetic averaging admit no analytical solution and must therefore be evaluated numerically. Among the simplest approximations is the approach of Turnbull and Wakeman (1991).

The first step consists in computing the first two, non-centered moments of the continuous, arithmetic average in the BMS framework. Using Fubini’s theorem, the expectation is given by

|     |     |     |
| --- | --- | --- |
| E" 1 Z _T S_(_t_)_dt_#<br><br>_T_ <sub>0</sub> | \=  | <sup>1 Z</sup> _<sup>T</sup>_ E\[_S_(_t_)\]_dt_<br><br>_T_ <sub>0</sub> |
|     | \=  | 1 Z _T_<br><br>_<sub>Se</sub>_(_r−y_)_tdt_<br><br>_T_ <sub>0</sub> |
|     | \=  | _S_(0)_M_<sub>1</sub>_,_ |

with

_M_<sub>1</sub> \= _e_((_r<sub>r</sub>−<sub>−</sub>y_)_T<sub>y</sub>_)_−<sub>T</sub>_<sup>1</sup>_._

A similar calculation (left as an exercise) shows that



E 1 Z _T S_(_t_)_dt_!2 = _S_2(0)_M_2_,_

_T_ <sub>0</sub>

with

 \[ \]

_M_<sub>2</sub> \=

+(_r <sub>−</sub>_2_y_)_T_<sup>2</sup> 2(_r <sub>−</sub>_1_y_) + _σ_<sup>2</sup> _<sup>−</sup> <sub>r −</sub>e_(_ry−_+_y_)_Tσ_<sup>2</sup> !_<sup>.</sup>_

In the next step, we match these first two, non-centered moments with the ones of the GBM. Specifically, in the BMS framework

E<sup>Q</sup> \[_S_(_T_)\] = _S_(0)_e_<sup>(</sup>_<sup>r−y</sup>_<sup>)</sup>_<sup>T</sup> ,_

EQ<sup>h</sup>_<sub>S</sub>_2(_<sub>T</sub>_)<sup>i</sup> \= _<sub>S</sub>_2(0)_<sub>e</sub>_\[2(_r−y_)+_σ_<sup>2</sup>\]_T <sub>.</sub>_

Hence the matching consists in finding parameters _<sub>ya</sub>_ and _<sub>σa</sub>_ such that

_e_(_r−ya_)_T_ \= _M_<sub>1</sub>_, e__._

|     |     |     |
| --- | --- | --- |
| The solution of that system is |     |     |
| _y_ | \=  | ln_M_<br><br>_r −_ <sup>1</sup> _,_ |

_<sub>a</sub>_

_T_

ln

_M_

2

_−_

2(

_r_

_−_

_y_

)

_._

s

_σ<sub>a</sub>_ \= _a_

_T_ The Turnbull and Wakeman (1991) then consists in valuing the arithmetic Asian option with the standard BMS formulae for European options using _<sub>ya</sub>_ and _<sub>σa</sub>_ as input convenience yield and volatility parameters, respectively.

**5.3 Lookback options**

Another important group of exotic options are the lookback options, sometimes referred to as the “no regret” options. The terminal payoff is defined according to the most advantageous historical outcome for the UA price. For instance, the fixed strike lookback call offers upon maturity

!

_,_

where \[_<sub>T</sub>_<sub>1</sub>_<sub>,T</sub>_<sub>2</sub>\] _<sub>⊆</sub>_ \[0_<sub>,T</sub>_\] is the period of observation for the UA price extremum. Similarly, the terminal payoff of the floating strike lookback call is

!

 _._

Thus, in contrast to barrier or Asian options, lookback options are not designed to reduce the cost of hedging. On the contrary, they offer an enhanced (and therefore more expensive) protection compared to vanilla options.

Goldman et al. (1979) and Conze and Viswanathan (1991b) derive some analytical solutions to lookback options in the BMS framework. Let _<sub>S</sub>_<sub>max</sub> and _<sub>S</sub>_<sub>min</sub> denote the maximum and minimum UA prices observed to date (i.e., when the derivative is evaluated). The BMS premium of the floating strike lookback call is

_cflo_ \= _S_(0)_e−yT_ Φ(_a_1) _− S_(0)_e−yT_ 2(_rσ−_2 _y_)Φ(_−a_1) _lookback_

_−S e_ _σ_2 _Y_ Φ(_−a_3)!_,_ min _a_2) _−_ 2(_r − y_)_e_

_−rT_ Φ(

where

ln

_S_

(0)

_S_

min

+

_r_

_y_

+

_σ_

2

2

_σ_

_√_

_T_

_,_

ln

_S_

(0)

_S_

min

+

_−_

_r_

+

_y_

+

_σ_

2

2

_T_

_√_

_a_

\=

_a_

1

_−_

_σ_

_T,_

\=

_−_

2

(

_r_

_−_

_y_

_−_

_σ_

2

2

)

ln

_S_

(0)

_S_

min

_σ_

2

_− T √ a_1 =2 _a_<sub>3</sub> \=_, Y._

_σ T_

The BMS premium of the floating strike lookback put is

_σ_2 _Z_Φ(_−b_3)!

_pflolookback_ \= _S_max_e−rT_ Φ(_b_1) _−_ 2(_r − y_)_e_

+_S_(0)_e−yT_ 2(_rσ−_2 _y_)Φ(_−b_2) _− S_(0)_e−yT_ Φ(_b_2)_,_

where

ln _SS_max(0) 2 _T √_

 _b_<sub>1</sub> \= _√ , b_<sub>2</sub> \= _b_<sub>1</sub> _− σ T,_

_b_<sub>3</sub> \=_, Z._

_σ T_

Cheuk and Vorst (1997) and Babbs (2000) develop a tree algorithm to evaluate lookback options when the extremum UA price is monitored in discrete time.

**5.4 Spread options**

This type of options is often used in commodity markets. Indeed, many traders are interested in taking a position into the difference between the input and the output of the commodity’s production process.

Examples include the so-called ”crack” spread (price difference between crude oil and refined petroleum), or the ”spark” spread (price difference between electricity and its production cost using natural gas). The terminal payoff of the spread call is

max(_S_<sub>1</sub>(_T_) _− S_<sub>2</sub>(_T_) _− K,_0)_,_

where _<sub>S</sub>_<sub>1</sub> and _<sub>S</sub>_<sub>2</sub> are two price processes representing the two legs of the spread.

As mentioned earlier, the linear combination of log-normal variables is not log-normally distributed. Hence, there are no explicit solutions for the pricing of spread options in the BMS framework. Analytical approximations can be found in Kirk (1995), Carmona and Durrleman (2003), or Bjerksund and Stensland (2014).

One particular case is when _<sub>K</sub>_ \= 0 and the spread option becomes an _exchange option_. The BMS closedform solution for that derivative was initially derived by Margrabe (1978). The payoff upon maturity is

max(_S_<sub>1</sub>(_T_) _− S_<sub>2</sub>(_T_)_,_0)_._

Consider an economy where asset _<sub>S</sub>_<sub>2</sub> is the _num´eraire_. In this economy, the terminal payoff of the exchange option is valued as

max_SS_<sub>2</sub>1((_TT_)) _−_ 1_,_0_,_

which can be interpreted as the terminal payoff of the European call written on asset _<sub>S</sub>_<sub>1</sub>_<sub>/S</sub>_<sub>2</sub> with strike 1. We can therefore readily apply the BMS pricing formula. But a crucial remark is that the risk-free rate is nil in this economy (since any position is rewarded through the appreciation of _<sub>S</sub>_<sub>2</sub>). Thus, denoting by _<sub>g</sub>_ the premium for the exchange option, the correct application of the BMS pricing formula yields

(0)_ge−y_2_T_ \= _SS_12(0)(0)_ee−−yy_12_TT_ Φ(_d_1) _−_ Φ(_d_2)_,_

_S_2

that is,

_g_ \= _S_1(0)_e−y_1_T_ Φ(_d_1) _− S_2(0)_e−y_2_T_ Φ(_d_2)_,_

with

 _d_1 = ln _S_21(0)(0)+ _y√−y_ +_σ_2 _T , d_2 = _d_1 _− σ√T,_

_σ T_

and _<sub>σ</sub>_<sup>2</sup> stands for the variance of the returns on _<sub>S</sub>_<sub>1</sub>(_<sub>t</sub>_)_<sub>/S</sub>_<sub>2</sub>(_<sub>t</sub>_).

To compute _<sub>σ</sub>_, we apply Itˆo’s lemma to the process _<sub>X</sub>_(_<sub>t</sub>_) := _<sub>S</sub>_<sub>1</sub>(_<sub>t</sub>_)_<sub>/S</sub>_<sub>2</sub>(_<sub>t</sub>_)

_dX_ ) + \[terms in _<sub>dt</sub>_\]_<sub>,</sub>_

or, alternatively,

 _dX_((_tt_)) _dS_ (_t_) _dS_ (_t_) + \[terms in _dt_\]_._

_X_

Stochastic terms in _<sub>dX</sub>_(_<sub>t</sub>_)_<sub>/X</sub>_(_<sub>t</sub>_) are therefore

_σ_1_dW_1_t − σ_2_dW_2_t._

Thus, if the two Brownian motions are correlated with correlation coefficient _<sub>ρ</sub>_, then

_σ_2 = _σ_12 + _σ_22 _−_ 2_σ_1_σ_2_ρ._

**5.5 Compound options**

These are by definition options on options. They can be useful hedging tools when the agent holds a conditional position (and therefore the need for hedging might appear in the future). A standard example relates to the tender process typically used in international trade. Among the bidders that participate in the tender to sell a product or a service to a foreign partner, the winner will enter into a long position in foreign currency. Hence all tender participants might want to hedge with a call on a put on the currency. Such a strategy is clearly a combination of speculation and hedging. If the tender is won, the call can be exercised (if ITM) to obtain the hedging put or it can be abandoned if an alternative hedging strategy is preferred (e.g., more favorable forward currency rate). If the tender is lost, the call can nevertheless be exercised if it is ITM (and the bidder can make a profit out of the strategy).

Consider the call with strike _<sub>K</sub>_<sub>1</sub> and maturity _<sub>T</sub>_<sub>1</sub>, written on the call with strike _<sub>K</sub>_<sub>2</sub> and maturity _<sub>T</sub>_<sub>2</sub> (both calls are European). The BMS pricing formula was initially derived by Geske (1977, 1979)

_ccall_ (0_,T_1_,T_2_,K_1_,K_2) = _S_(0)_e−yT_2Φ2 _a_1_,b_1_,_q_T_1_/T_2

_−K_2_e−rT_2Φ2 _a_2_,b_2_,_q_T_1_/T_2 _− K_1_e−rT_1Φ(_a_2)_,_

with

ln _SS_(0)_~~∗~~_ +_r−y_+_σ_22 _T_1 _√_

_a_<sub>1</sub> \= _√ , a_<sub>2</sub> \= _a_<sub>1</sub> _− σ_

_T_

1

_,_

_b_1 = _σ T_2 _, b_2 = _b_1 _− σ√T_2_,_

_σ_

_T_

1

ln

_S_

(0)

_K_

2

+

_r_

_−_

_y_

+

_σ_

2

2

_T_

2

_√_

and _<sub>S</sub><sup>∗</sup>_ is the UA price level such that the underlying call is ATM, i.e.,

_c_(_T_<sub>1</sub>_,T_<sub>2</sub>_,K_<sub>2</sub>_|S_ \= _S<sup>∗</sup>_) = _K_<sub>1</sub>_._

In the above formula, the function Φ<sub>2</sub> (_<sub>x,y,ρ</sub>_) is the cumulative distribution function of the bivariate standard normal law. In other words, it is the joint probability that the draw from one standard normal variable is smaller than _<sub>x</sub>_ while the draw from another standard normal variable is smaller than _<sub>y</sub>_, when the two variables are correlated with correlation coefficient _<sub>ρ</sub>_. An algorithm for approximating that function can be found in Basu and Hull (2021). Alternatively, Φ<sub>2</sub> (_<sub>x,y,ρ</sub>_) can be valued from numerical integration using

Z _x_ _y − ρu_ !

Φ2 (_x,y,ρ_) = _ϕ_(_u_)Φ p1 _− ρ_2 _du._

_−∞_

The pricing formula for the call on the call can be interpreted as follows. The option eventually gives right to a long position in _<sub>S</sub>_ provided the two calls end up ITM and the two strikes are paid. The first strike _K_<sub>1</sub> is paid only if the underlying call ends up ITM. This has a probability of Φ(_<sub>a</sub>_<sub>2</sub>). The second strike _<sub>K</sub>_<sub>2</sub> is paid only if _S_(_T_<sub>1</sub>) _≥ S<sup>∗</sup>_ and _S_(_T_<sub>2</sub>) _≥ K_<sub>2</sub>. This has a probability of Φ<sub>2</sub> _a_<sub>2</sub>_,b_<sub>2</sub>_,_<sup>p</sup>_T_<sub>1</sub>_/T_<sub>2</sub>. Indeed, the same Brownian motion is driving _<sub>S</sub>_(_<sub>T</sub>_<sub>1</sub>) and _<sub>S</sub>_(_<sub>T</sub>_<sub>2</sub>). From date 0 till _<sub>T</sub>_<sub>1</sub>, that source of risk is perfectly correlated with itself. From _<sub>T</sub>_<sub>1</sub> to _<sub>T</sub>_<sub>2</sub>, the path of the Brownian motion is fully independent from its behavior from date 0 till _<sub>T</sub>_<sub>1</sub>. Hence, the overall correlation between the two conditions is <sup>p</sup>_<sub>T</sub>_<sub>1</sub>_<sub>/T</sub>_<sub>2</sub>. Finally, as in the univariate case, the probability factor associated with the UA price is adjusted to Φ<sub>2</sub> _<sub>a</sub>_<sub>1</sub>_<sub>,b</sub>_<sub>1</sub>_<sub>,</sub>_<sup>p</sup>_<sub>T</sub>_<sub>1</sub>_<sub>/T</sub>_<sub>2</sub> to account for the correlation between the payoff in _<sub>S</sub>_ and the moneyness condition.

Applying that same logic, the BMS formulae for the call on the put, the put on the call, and the put on the put are respectively given by

_cput_ (0_,T_1_,T_2_,K_1_,K_2) = _K_2_e−rT_2Φ2 _−a_2_,−b_2_,_q

_T_

1

_/T_

2

_−S_(0)_e−yT_2Φ2 _−a_1_,−b_1_,_q_T_1_/T_2 _− K_1_e−rT_1Φ(_−a_2)_,_

q

_T_

1

_/T_

2

_pcall_ (0_,T_1_,T_2_,K_1_,K_2) = _K_2_e−rT_2Φ2 _−a_2_,b_2_,−_

_−S_(0)_e−yT_2Φ2 _−a_1_,b_1_,−_q_T_1_/T_2 + _K_1_e−rT_1Φ(_−a_2)_,_

_p<sub>put</sub>_ (0_,T_<sub>1</sub>_,T_<sub>2</sub>_,K_<sub>1</sub>_,K_<sub>2</sub>) = _S_(0)_e−yT_2Φ2 _a_1_,−b_1_,−_q_T_1_/T_2

_−K_2_e−rT_2Φ2 _a_2_,−b_2_,−_q_T_1_/T_2 + _K_1_e−rT_1Φ(_a_2)_._

**5.6 Options on the minimum or maximum of two assets**

Stulz (1982) examines these options in the BMS framework. For instance, the European call on the minimum yields the following terminal payoff

max(min(_S_<sub>1</sub>(_T_)_,S_<sub>2</sub>(_T_)) _− K,_0)_._

Note that when _<sub>K</sub>_ \= 0, such options can be directly evaluated using the price of an exchange option since

max(_S_<sub>1</sub>(_T_)_,S_<sub>2</sub>(_T_)) = _S_<sub>1</sub>(_T_) + max(_S_<sub>2</sub>(_T_) _− S_<sub>1</sub>(_T_)_,_0)_,_ min(_S_<sub>1</sub>(_T_)_,S_<sub>2</sub>(_T_)) = _S_<sub>2</sub>(_T_) _−_ max(_S_<sub>2</sub>(_T_) _− S_<sub>1</sub>(_T_)_,_0)_._

In the general case where _<sub>K ></sub>_ 0, the terminal payoff of the call on the minimum can be written as

_S_1(_<sup>T</sup>_)1_K<S_<sub>1</sub>(_T_)_<S_<sub>2</sub>(_T_) + _S_2(_<sup>T</sup>_)1_K<S_<sub>2</sub>(_T_)_<S_<sub>1</sub>(_T_) _− <sup>K</sup>_1_S_<sub>1</sub>(_T_)_\>K_1_S_<sub>2</sub>(_T_)_\>K._

The first term can be simplified into

_S_1(_T_)1_K<S_1(_T_)_<S_2(_T_) = _S_1(_T_)1_S_2(_T_)_\>_11_S_1(_T_)_\>K._

_S_1(_T_)

The first indicator function corresponds to the event that the exchange option is ITM. As shown earlier, this event has a probability

 _T_ 

ln

_S_

2

(0)

_S_

1

(0)

_−_

_σ_

2

2

_√_

Φ<sub></sub> := Φ(_d_<sub>2</sub> (_σ_))_._

_σ T_

The second indicator function corresponds to the event that the vanilla call written on _<sub>S</sub>_<sub>1</sub> is ITM. This event has a probability

 

_T_

Φ _√_  := Φ(_d_<sub>2</sub> (_σ_<sub>1</sub>))_._

 _σ_<sub>1</sub> _T_ 

The joint probability of these two events is

Φ<sub>2</sub> _d_<sub>2</sub> (_σ_<sub>1</sub>)_,d_<sub>2</sub> (_σ_)_,ρ<sup>′</sup>,_

where _<sub>ρ</sub><sup>′</sup>_ stands for the correlation coefficient between the returns on _<sub>S</sub>_<sub>1</sub> and those on _<sub>S</sub>_<sub>2</sub>_<sub>/S</sub>_<sub>1</sub>. By analogy with the proof of the BMS formula for the vanilla call, we obtain

E _e rT S__,ρ′,_

with

_<sup>K</sup>_ <sup>2</sup> _T_

_d_<sub>1</sub> (_σ_<sub>1</sub>) := _√ ._

_σ_<sub>1</sub> _T_

To determine _<sub>ρ</sub><sup>′</sup>_, note that the product of the processes _<sub>S</sub>_<sub>2</sub>(_<sub>t</sub>_)_<sub>/S</sub>_<sub>1</sub>(_<sub>t</sub>_) and _<sub>S</sub>_<sub>1</sub>(_<sub>t</sub>_) has a return variance _<sub>σ</sub>_<sub>2</sub><sup>2</sup>.

But the return variance of that product can also be written as

_σ_2 + _σ_12 + 2_σσ_1_ρ′._

Hence

_ρ<sup>′</sup>_ \= _._

By substituting _<sub>S</sub>_<sub>1</sub> and _<sub>S</sub>_<sub>2</sub>, we get

E _e rT S__,ρ′′,_

with

<sub>2</sub>(0)

ln

_S_

_K_

+

_r_

+

_σ_

2

2

2

_T_

_√_

_d_<sub>1</sub> (_σ_<sub>2</sub>) = _, ρ_ _,_

_σ_<sub>2</sub> _T_ and

_<sup>′</sup>_ (_σ_) = ln _SS_21(0)(0)_√− σ_22_T . d_<sub>2</sub>

_σ T_

Finally, regarding the last term, _<sub>K</sub>_1_<sub>S</sub>_<sub>1(</sub>_<sub>T</sub>_<sub>)</sub>_<sub>\>K</sub>_1_<sub>S</sub>_<sub>2(</sub>_<sub>T</sub>_<sub>)</sub>_<sub>\>K</sub>_, the two indicator functions correspond to the event that the call written on _<sub>S</sub>_<sub>1</sub> and the one written on _<sub>S</sub>_<sub>2</sub> are both ITM. Which yields

E _e <sup>rT</sup> K__._

Combining all these results, we obtain the premium of the call on the minimum

_c<sub>min</sub>_(0_,T,K_) = _S_<sub>1</sub>(0)Φ<sub>2</sub> _d_<sub>1</sub> (_σ_<sub>1</sub>)_,d_<sub>2</sub> (_σ_)_,ρ<sup>′</sup>_ \+ _S_<sub>2</sub>(0)Φ<sub>2</sub> _d_<sub>1</sub> (_σ_<sub>2</sub>)_,d<sup>′</sup>_<sub>2</sub> (_σ_)_,ρ<sup>′′</sup>_ _−Ke<sup>−rT</sup>_ Φ<sub>2</sub> (_d_<sub>2</sub> (_σ_<sub>1</sub>)_,d_<sub>2</sub> (_σ_<sub>2</sub>)_,ρ_)_._

The premiums of all other options on minimum or maximum of two assets can be derived in a similar fashion.

**5.7 Miscellaneous exotic options**

In this section we briefly mention some other commonly encountered exotic options.

#### 5.7.1 Bermudian options

This name refers to a type of American options where the early exercise right is restricted to a limited number of pre-specified dates. Bermudian options can be written on coupon bearing bonds, for example. In that case, the most relevant times for exercising the option is on coupon dates.

#### 5.7.2 Chooser options

Such options, a.k.a. ”as you like it options”, give the right to choose between a call or a put. Let _<sub>Tc</sub>_ denote the expiry date of the chooser option. The corresponding payoff upon maturity is

max(_C_ (_T<sub>c</sub>,T_<sub>1</sub>_,K_<sub>1</sub>)_,P_ (_T<sub>c</sub>,T_<sub>2</sub>_,K_<sub>2</sub>))_._

When the underlying options are European, _<sub>T</sub>_<sub>1</sub> \= _<sub>T</sub>_<sub>2</sub> and _<sub>K</sub>_<sub>1</sub> \= _<sub>K</sub>_<sub>2</sub>, the chooser option can be decomposed into vanilla options. Indeed, using the put-call parity

max(_c_(_T<sub>c</sub>,T_<sub>1</sub>_,K_<sub>1</sub>)_,p_(_T<sub>c</sub>,T_<sub>1</sub>_,K_<sub>1</sub>))

\= max_c_(_Tc,T_1_,K_1)_,c_(_Tc,T_1_,K_1) _− S_ (_Tc_) + _K_1_e−r_(_T_1_−Tc_) = _c_(_Tc,T_1_,K_1) + max_K_1_e−r_(_T_1_−Tc_) _− S_ (_Tc_)_,_0_._

So the chooser option today is worth

_c_(0_,T_1_,K_1) + _p_0_,Tc,K_1_e−r_(_T_1_−Tc_)_._

#### 5.7.3 Shout options

In the shout option contract, the holder has the right to reset the strike at the UA price current level (i.e., the option restarts ATM). There is usually only one right to ”shout”, but it is possible to include several shouts in the contract. Shouts can only be exercised when the option is ITM.

Consider for example the shout call with strike _<sub>K</sub>_. If the holder decides to shout at date _<sub>τ</sub>_ (it must be that _<sub>S</sub>_(_<sub>τ</sub>_) _<sub>\> K</sub>_), then he or she receives the monetary amount _<sub>S</sub>_(_<sub>τ</sub>_) _<sub>− K</sub>_ and is now long the call with strike _<sub>S</sub>_(_<sub>τ</sub>_). At time _<sub>τ</sub>_ the value of the shout call is therefore

E<sup>Q</sup> \[max(_S_(_T_) _− S_(_τ_)_,_0)\]_e<sup>−r</sup>_<sup>(</sup>_<sup>T−τ</sup>_<sup>)</sup> \+ _S_(_τ_) _− K._

Like American options, the valuation of this type of option relies on the determination of the optimal shout policy.

**5.8 Problem set**

#### Exercise 5.1

The paylater call is a European option to buy the UA where the premium _<sub>π</sub>_ is paid only if the option ends up ITM. Thus, the initial cost of that option is nil and its terminal payoff is

<sup>(</sup> _S_ (_T_) _− K − π_ if _S_ (_T_) _≥ K,_

0 otherwise.

In the BMS framework, compute the value of _<sub>π</sub>_ in the AoA as a function of the European call premium _c_(0_,T,K_)).

#### Exercise 5.2

The European put written on _<sub>S</sub>_, with maturity _<sub>T</sub>_ and strike $150 is worth $22. In the AoA, how much should cost the down&in put with same characteristics and activating barrier set at $160?

#### Exercise 5.3

The power option offers the terminal payoff

max_<sub>S</sub>_<sup>2</sup>(_T_) _−_ 900_,_0_<sub>.</sub>_

The current UA price is _<sub>S</sub>_ \= 30 and the risk-free rate is _<sub>r</sub>_ \= 5%. There are no dividends. (a) Suppose you evaluate the option using the binomial tree below

_S_(_<sub>T</sub>_) = 36

_S_(0) = 30

_S_(_<sub>T</sub>_) = 25

Set _<sub>T</sub>_ \= 1 year.

What is the risk-neutral probability that the UA price is 36 at date _<sub>T</sub>_? What is the current value of the power option?

1.  Suppose now you evaluate the option in the BMS framework. Let _<sub>σ</sub>_ denote the volatility of the UA returns. Expressing the UA price as the solution to the GBM, show that for any time _<sub>t</sub>_

_S_2(_t_) = _S_2(0)exp" _R −_ Σ22 !_t_ \+ Σ_Wt_#_,_

where _<sub>R</sub>_ and Σ are two constants to be determined.

1.  Using the analogy with the BMS formula for the European call, and making the appropriate adjustments, provide a solution to the pricing of the power option.
2.  Compute the BMS value of the power option when the volatility parameter is set so as to make the binomial tree a CRR tree (thereby guaranteeing the convergence of the discrete time solution to the continuous time solution).

#### Exercise 5.4

Consider the European-type exotic option with terminal payoff

max(0;min(_U − S_(_T_);_U − L_))_,_

where _<sub>U</sub>_ and _<sub>L</sub>_ (_<sub>< U</sub>_) are positive constants.

1.  Show that the terminal payoff can be rewritten as the payoff of a combination of European puts.
2.  Show that the terminal payoff can be rewritten as the payoff of a combination of European calls plus a cash flow.
3.  Deduce the BMS value of the exotic option.
4.  Compute the delta and the gamma of the exotic option. Show that the sign of the gamma changes at some critical UA price level. Why is it so?

#### Exercise 5.5

The XYZ stock is quoted at 100 and does not pay any dividend within the next 3 months. The return volatility is estimated at 20%. The risk-free rate is 5%.

1.  Using the CRR tree with a monthly time step, compute the value of the European call written on XYZ, with strike 100 and 3-month maturity.
2.  Using the same tree, compute the value of the European lookback call where the floating strike price is the lowest XYZ price observed from _<sub>t</sub>_ \= 0 till _<sub>T</sub>_ \= 3 months (observation frequency is monthly). Compare with the preceding result.
3.  Suppose the observation frequency is weekly. Will it increase or decrease the value of the lookback call? Explain.

#### Exercise 5.6

(Cheuk and Vorst (1997)) Consider a European lookback call with maturity _<sub>T</sub>_, whose terminal payoff is: _L_(_T_) = _S_(_T_) _− M_(_T_) where _M_(_T_) = min _S_(_t_)_._

_t∈_\[0_,T_\]

The underlying asset is currently worth _<sub>S</sub>_(0) and does not pay dividends. The asset’s returns volatility is denoted _<sub>σ</sub>_ and the risk-free rate is _<sub>r</sub>_.

You want to derive a version of the binomial tree (with _<sub>N</sub>_ time steps) that will allow you to evaluate _L_ in a recombining tree. To that end, you first consider the risk-adjusted probabilities _<sub>q</sub>_ and 1_<sub>−q</sub>_, as well as the values of _<sub>u</sub>_ and _<sub>d</sub>_ as defined by CRR. However, you will change the state variable. In the CRR binomial tree, the state variable at time step _<sub>n</sub>_ is the value of the underlying after _<sub>n</sub>_ steps. Here, the state variable will be _<sub>k</sub>_ such that the minimum encountered so far is given by:

_Mn_(_k_) = _Sndk_ where _Sn_ \= _S_0_un−jdj_

1.  Show that the the payoff _<sub>LN</sub>_(_<sub>k</sub>_), after the _<sub>N</sub>_ time steps in the tree, is given by:

_L<sub>N</sub>_(_k_) = _S<sub>N</sub>V<sub>N</sub>_(_k_)_,_

where _V<sub>N</sub>_(_k_) = (1 _− d<sup>k</sup>_).

1.  Given _r_, _q_, _L<sub>n</sub>_(_·_) and _V<sub>n</sub>_(_·_), _n >_ 0, describe the value of _L<sub>n−</sub>_<sub>1</sub>(_k_) as a function of (i) _S<sub>n−</sub>_<sub>1</sub> and (ii) _V<sub>n−</sub>_<sub>1</sub>(_<sub>k</sub>_), whose value is to be determined.
2.  Demonstrate that the expectation in (b) can be rewritten as a function of modified probabilities _q_˜ = _<sub>e</sub><sup>−r</sup>_<sup>∆</sup>_<sup>t</sup><sub>qu</sub>_ and 1 _− <sub>q</sub>_˜. Comment on the expression of _<sub>Vn−</sub>_<sub>1</sub>(_<sub>k</sub>_) under this new measure; what is particular about it?

#### Exercise 5.7

The cumulative return _<sub>R</sub>_(_<sub>t</sub>_) on a financial asset is assumed to be driven by the following EMM dynamics:

_dR_(_t_) = _σdW<sub>t</sub>,_

where _<sub>Wt</sub>_ is a standard Brownian motion.

1.  Write down the solution for _<sub>R</sub>_(_<sub>t</sub>_).

A derivative instrument pays $1 at date _<sub>T</sub>_ if the following two conditions are met:

- 1.  The cumulative return reaches the upper bound _<sub>H > R</sub>_(0) before _<sub>T</sub>_,
    2.  The cumulative return at time _<sub>T</sub>_ is below the lower bound _<sub>K < R</sub>_(0).

1.  Using the reflection principle, compute the probability under the EMM that the derivative pays $1.
2.  Determine the initial value of that derivative (let _<sub>r</sub>_ denote the risk-free rate).

#### Exercise 5.8

Let _<sub>θ</sub>_ denote the first time the standard Brownian motion hits level _<sub>y ></sub>_ 0, that is

_θ_ \= inf _{t ≥_ 0 : _W<sub>t</sub>_ \= _y}._

1.  Using a simple reasoning, compute Proba(_<sub>θ < T,WT</sub> \> <sub>y</sub>_).
2.  Using the reflection principle, compute Proba(_<sub>θ < T,WT</sub> < <sub>y</sub>_).
3.  Establish that Proba( where Φ(_<sub>.</sub>_) stands for the normal cdf.

_θ<_

_T_

)=2Φ

_−_

_y_

_√_

_T_

1.  Compute the value of the derivative that pays $1 at time _<sub>T</sub>_ if the maximum value of the Brownian motion between now and _<sub>T</sub>_ has not reached the level _<sub>y</sub>_.

#### Exercise 5.9

Asian option on average strike (adapted from Dewynne and Wilmott, 1995). Let _<sub>M</sub>_(_<sub>t</sub>_) denote the continuous arithmetic average of the UA price

_M_(_t_) = 1 <sup>Z</sup> _<sup>t</sup> <sub>S</sub>_(_u_)_du. t_ 0

The Asian call yields the following terminal payoff

max(_S_(_T_) _− M_(_T_)_,_0)_._

(a) Consider the portfolio made of a long position in the Asian call and a short position in the corresponding Asian put. What is the value of that portfolio at time _<sub>T</sub>_? (b) Show that the put-call parity at time 0 is (hint: Use Fubini’s theorem)

_cAsian_(0_,T,M_(_T_)) _− p<sub>Asian</sub>_(0_,T,M_(_T_)) = _S_(0) _− <sup>S</sup>_<sup>(0)</sup> 1 _− e<sup>−rT</sup> . rT_ (c) For a given date _<sub>t</sub>_ between 0 and _<sub>T</sub>_, show that the put-call parity is now

_cAsian_(_t,T,M_(_T_)) _− pAsian_(_t,T,M_(_T_)) = _S_(_t_) _− S_(_t_) 1 _− e−r_(_T−t_) _−_ 1 _e−r_(_T−t_) Z _t S_(_u_)_du,_

_rT T_ <sub>0</sub>

(recall the average is calculated since date 0).

#### Exercise 5.10

Consider two assets _<sub>x</sub>_ and _<sub>y</sub>_. Portfolio _<sub>A</sub>_ contains the European option to exchange asset _<sub>y</sub>_ against asset _<sub>x</sub>_ with terminal payoff max(_<sub>x</sub>_(_<sub>T</sub>_) _<sub>− y</sub>_(_<sub>T</sub>_);0). Portfolio _<sub>B</sub>_ contains a long position in _<sub>x</sub>_ and a short position in _<sub>y</sub>_.

1.  Show that, for any date _<sub>t ≤ T</sub>_, the value of portfolio _<sub>A</sub>_ is greater than the value of portfolio _<sub>B</sub>_.
2.  What can you say about the value of the American exchange option?

#### Exercise 5.11

A rainbow option is a derivative whose payoff is related to two (or more) correlated assets. The goal is to evaluate a simple version of the rainbow option. Let _<sub>Z</sub><sup>a</sup>_(_<sub>t</sub>_) and _<sub>Z</sub><sup>b</sup>_(_<sub>t</sub>_) denote two standard Brownian motions such that d_<sub>Z</sub><sup>a</sup>_(_<sub>t</sub>_) _<sub>·</sub>_ d_<sub>Z</sub><sup>b</sup>_(_<sub>t</sub>_) = _<sub>ρdt</sub>_. A third stochastic process _<sub>W</sub>_(_<sub>t</sub>_), independent from _<sub>Z</sub><sup>a</sup>_(_<sub>t</sub>_), is defined as

_Z<sup>b</sup>_(_t_) = _ρZ<sup>a</sup>_(_t_) + <sup>q</sup>1 _− ρ_<sup>2</sup>_W_(_t_)_._

1.  Show that _<sub>W</sub>_(_<sub>t</sub>_) is a Brownian motion.

A European-style rainbow option yields the following payoff

<sup>(</sup> _B_(_T_) if _A_(_T_) _≥ K,_

0 if _A_(_T_) _< K,_

where _<sub>A</sub>_ and _<sub>B</sub>_ are two traded assets with EMM dynamics

d_AA_((_t_)_t_) = _r_d_t_ \+ _σa_ d_Za_(_t_)_, dBB_((_tt_)) = _rdt_ \+ _σb_ d_Zb_(_t_)_._

1.  Compute the premium for the rainbow option.

#### Exercise 5.12

The Russian option is a perpetual option that can be exercised at any time. The payoff upon exercise is the historical maximum of the UA price. Let _<sub>M</sub>_ denote the historical maximum of the UA price observed until now. The value of the Russian option depends on the current UA price _<sub>S</sub>_ and on _<sub>M</sub>_. Also, denote by _S<sup>∗</sup>_ the optimal exercise threshold. Assume the BMS framework and use the standard notations _<sub>r</sub>_, _<sub>y</sub>_ and _σ_ for the risk-free rate, the convenience yield and the volatility, respectively.

1.  Recall the ODE followed by the value of the Russian option _<sub>g</sub>_ \= _<sub>g</sub>_ (_<sub>S,M</sub>_) in the domain _<sub>S</sub><sup>∗</sup> <sub>< S < M</sub>_.
2.  Noting that _<sub>M</sub>_ can be treated as a parameter, use the following change of variable

_S_

_X_ \= _,_

_M_

and show that the ODE for _<sub>g</sub>_ (_<sub>X</sub>_) becomes

_._

1.  Show that the general solution of that ODE is

_g_ (_X_) = _aX<sup>λ</sup>_<sup>1</sup> \+ _bX<sup>λ</sup>_<sup>2</sup>_,_

where _<sub>λ</sub>_<sub>1</sub> and _<sub>λ</sub>_<sub>2</sub> are the two roots of the characteristic polynomial, i.e.,

_λ_<sub>1</sub> \= 12 _−_ _r − y − σ_22 ! _−_ s 2 

_r_

_−_

_y_

_−_

_σ_

2

2

2

+2

_σ_

_r_

_,_

_r_

_−_

_y_

_−_

_σ_

2

2

_σ_

_λ_<sub>2</sub> \= 12 _−_ _r − y − σ_22 ! + s 2 + 2_σ_2_r__._

_σ_

1.  The boundary conditions defining the Russian option are as follows: (i) when _<sub>X</sub>_ \= _<sub>X</sub><sup>∗</sup>_ \= _<sub>S</sub><sup>∗</sup><sub>/M</sub>_, then _g_ (_<sub>X</sub><sup>∗</sup>_) = 1, and (ii) when _<sub>X</sub>_ \= 1, the UA price has reached its maximum to date and therefore

_∂g_ (_X_)

_∂X X_

Use these two boundary conditions to determine the constants _<sub>a</sub>_ and _<sub>b</sub>_.

1.  Combining that result with the generic solution, show that the value of the Russian option is given by

_g_ _._

Determine the optimal exercise policy _<sub>X</sub><sup>∗</sup>_.

**5.9 Solutions**

#### Solution 5.1

In the AoA the premium _<sub>π</sub>_ verifies

_e−rT_ EQh(_S_(_T_) _− K − π_)1_S_(_T_)_≥K_i = 0_,_

which yields

_e−rT_ EQh(_S_(_T_) _− K_)1_S_(_T_)_≥K_i _− πe−rT_ EQh1_S_(_T_)_≥K_i = 0_._

Hence

_erT π_ \= Φ(_<sub>d</sub>_2)_c_(0_,T,K_)_._

**Solution 5.2**

$22.

#### Solution 5.3

1.  The risk-neutral probability _<sub>q</sub>_ is such that

(_q ×_ 36 + (1 _− <sub>q</sub>_)25)_e<sup>−</sup>_<sup>0</sup>_<sup>.</sup>_<sup>05</sup> \= 30_,_

which yields _<sub>q ≃</sub>_ 0_<sub>.</sub>_5944.

The value of the power option is then

_._

1.  The solution to the GBM is

" _σ_2 ! # _S_(_t_) = _S_(0)exp _r −_ 2 _t_ \+ _σW_(_t_) _._

Thus

_S_2(_t_) = _S_2(0)exp" _R −_ Σ22 !_t_ \+ Σ_W_(_t_)#_,_

with

Σ = 2_σ, R_ \= 2_r_ \+ _σ_<sup>2</sup> _._

1.  The UA _<sub>S</sub>_<sup>2</sup>(_<sub>t</sub>_) is driven by a GBM with convenience yield

_y_ \= _r − R_ \= _−r − σ_<sup>2</sup>_,_

and volatility 2_<sub>σ</sub>_. Hence the BMS valuation formula for the power option is

_S_2(0)_e_(_r_+_σ_2)_T_ Φ(_d_1) _− Ke−rT_ Φ(_d_2)_,_

with

ln _S_2(0) + 2_r_ \+ 3_σ_2 _d,_

ln _S_<sup>2</sup>(0) <sup>\+</sup> 2 _<sub>d</sub>_<sub>2</sub> \= _K <sub>√</sub>r − σ_2_T <sub>.</sub>_

2_σ T_

1.  To work with a CRR tree, one must set

_._

Which yields _<sub>g ≃</sub>_ 202.

#### Solution 5.4

1.  The terminal payoff is

max(0;min(_U − S_(_T_);_U − L_)) = (_U − S_(_T_))<sup>\+</sup> _−_ (_L − S_(_T_))<sup>\+</sup> _._

1.  From put-call parity, this can be rewritten as

_U − L_ \+ (_S_(_T_) _− U_)<sup>\+</sup> _−_ (_S_(_T_) _− L_)<sup>\+</sup> _._

1.  Consequently, the exotic option is worth

_Ue<sup>−rT</sup>_ Φ(_−d_<sub>2</sub>) _− S_(0)Φ(_−d_<sub>1</sub>) _− Le<sup>−rT</sup>_ Φ(_−d_<sub>4</sub>) + _S_(0)Φ(_−d_<sub>3</sub>)_,_

where

_S_(0) _<sub>σ</sub>_2

ln

_U_

2

_σ_

_√_

_T_

ln

_S_

(0)

_L_

+

_r_

+

_σ_

2

2

_T_

_√_

\+ _r_\+ _T √ d_<sub>1</sub> \=_, d_<sub>2</sub> \= _d_<sub>1</sub> _− σ T,_

_d_<sub>3</sub> \=_, d_<sub>4</sub> \= _d_<sub>3</sub> _− σ√T._

|     |     |
| --- | --- |
| (d) The delta and the gamma are given by | _σ T_ |
| ∆_<sub>g</sub>_ \= | _−_Φ(_−d_<sub>1</sub>) + Φ(_−d_<sub>3</sub>) _<_ 0_,_ |

exp

_−_

_d_

2

1

2

_−_

exp

_−_

_d_

2

3

2

_√_

_√_

Γ_<sub>g</sub>_ \=_._

_S_(0)_σ T_ ~~2~~_π_

There is a critical value for _<sub>S</sub>_ where the numerator is nil. Indeed, the condition _<sub>d</sub>_<sup>2</sup><sub>1</sub> \= _<sub>d</sub>_<sup>2</sup><sub>3</sub> is equivalent to

_S∗_ \= exp"21 ln_UL −_ _r_ \+ _σ_22 !_T_#_._

The exotic option is akin to a spread (long one put and short the other). Depending on the relative moneyness of the two options, the net gamma can be either positive or negative.

#### Solution 5.5

1.  Solution is _<sub>c</sub>_0_<sub>,</sub>_ <sup>1</sup><sub>4</sub>_,_100 \= 4_<sub>.</sub>_94433.
2.  The CRR tree generates the following eight paths

Path UA price Lowest price

|     |     |     |
| --- | --- | --- |
| _u − u − u_ | 100 _−_ 105_<sub>.</sub>_943 _−_ 112_<sub>.</sub>_24 _−_ 118_<sub>.</sub>_911 | 100 |
| _u − u − d_ | 100 _−_ 105_<sub>.</sub>_943 _−_ 112_<sub>.</sub>_24 _−_ 105_<sub>.</sub>_943 | 100 |
| _u − d − u_ | 100 _−_ 105_<sub>.</sub>_943 _−_ 100 _−_ 105_<sub>.</sub>_943 | 100 |
| _u − d − d_ | 100 _−_ 105_<sub>.</sub>_943 _−_ 100 _−_ 94_<sub>.</sub>_39 | 94_<sub>.</sub>_39 |
| _d − u − u_ | 100 _−_ 94_<sub>.</sub>_39 _−_ 100 _−_ 105_<sub>.</sub>_943 | 94_<sub>.</sub>_39 |
| _d − u − d_ | 100 _−_ 94_<sub>.</sub>_39 _−_ 100 _−_ 94_<sub>.</sub>_39 | 94_<sub>.</sub>_39 |
| _d − d − u_ | 100 _−_ 94_<sub>.</sub>_39 _−_ 89_<sub>.</sub>_0947 _−_ 94_<sub>.</sub>_39 | 89_<sub>.</sub>_0947 |
| _d − d − d_ | 100 _−_ 94_<sub>.</sub>_39 _−_ 89_<sub>.</sub>_0947 _−_ 84_<sub>.</sub>_0965 | 84_<sub>.</sub>_0965 |

therefore the lookback call offers the following payoffs

|     |     |     |
| --- | --- | --- |
| Path | Terminal payoff (_<sub>fi</sub>_) | Probability (_<sub>πi</sub>_) |
| _u − u − u_ | 118_<sub>.</sub>_911 _<sub>−</sub>_ 100 = 18_<sub>.</sub>_911 | _q_<sup>3</sup> \= 0_<sub>.</sub>_142 |
| _u − u − d_ | 105_<sub>.</sub>_943 _<sub>−</sub>_ 100 = 5_<sub>.</sub>_943 | _q_<sup>2</sup> (1 _− <sub>q</sub>_) = 0_<sub>.</sub>_1302 |
| _u − d − u_ | 105_<sub>.</sub>_943 _<sub>−</sub>_ 100 = 5_<sub>.</sub>_943 | _q_<sup>2</sup> (1 _− <sub>q</sub>_) = 0_<sub>.</sub>_1302 |
| _u − d − d_ | 94_<sub>.</sub>_39 _−_ 94_<sub>.</sub>_39 = 0 | _q_ (1 _− <sub>q</sub>_)<sup>2</sup> \= 0_<sub>.</sub>_11935 |
| _d − u − u_ | 105_<sub>.</sub>_943 _<sub>−</sub>_ 94_<sub>.</sub>_39 = 11_<sub>.</sub>_553 | _q_<sup>2</sup> (1 _− <sub>q</sub>_) = 0_<sub>.</sub>_1302 |
| _d − u − d_ | 94_<sub>.</sub>_39 _−_ 94_<sub>.</sub>_39 = 0 | _q_ (1 _− <sub>q</sub>_)<sup>2</sup> \= 0_<sub>.</sub>_11935 |
| _d − d − u_ | 94_<sub>.</sub>_39 _<sub>−</sub>_ 89_<sub>.</sub>_0947 = 5_<sub>.</sub>_2953 | _q_ (1 _− <sub>q</sub>_)<sup>2</sup> \= 0_<sub>.</sub>_11935 |
| _d − d − d_ | 84_<sub>.</sub>_0965 _<sub>−</sub>_ 84_<sub>.</sub>_0965 = 0 | (1 _− <sub>q</sub>_)<sup>3</sup> \= 0_<sub>.</sub>_1094 |

and its current value is

8

_clookback_ \= _e−_0_._405 X_fiπi,_

_i_\=1

which yields

_clookback_ \= 6_._29_._

Not surprisingly, _<sub>clookback</sub> \> <sub>c</sub>_(0_<sub>,T,K</sub>_) since the lookback call retains the most favorable conditions to set the strike price.

1.  With a weekly observation frequency, the lookback call becomes more valuable. Indeed, a higher observation frequency increases the chances of observing more extreme UA prices.

#### Solution 5.6

1.  We have

_L<sub>N</sub>_(_k_) = _S<sub>N</sub> − M<sub>N</sub>_(_k_)

\= _S<sub>N</sub>_(1 _− M<sub>N</sub>_(_k_)_/S<sub>N</sub>_)

\= _S<sub>N</sub>_(1 _− d<sup>k</sup>_)

Hence, _V<sub>N</sub>_(_k_) = (1 _− d<sup>k</sup>_).

1.  We have

_Ln−_1(_k_) = _e−r_∆_t_ h_qLn_(_k_ \+ 1) + (1 _− q_)_Ln_ (_k −_ 1)+i

\= _e−r_∆_t_ h_quSn−_1_Vn_(_k_ \+ 1) + (1 _− q_)_dSn−_1_Vn_ (_k −_ 1)+i

\= _Sn−_1_e−r_∆_t_ h_quVn_(_k_ \+ 1) + (1 _− q_)_dVn_ (_k −_ 1)+i

_⇒ V<sub>n−</sub>_<sub>1</sub>(_k_) = _e<sup>−r</sup>_<sup>∆</sup>_<sup>t</sup>_ <sup>h</sup>_quV<sub>n</sub>_(_k_ \+ 1) + (1 _− q_)_dV<sub>n</sub>_ (_k −_ 1)<sup>+i</sup>

1.  From b), we can write

_q_˜= _e−r_∆_tqu_ \= _e−r_∆_t er_∆_t − du_ \= _u − e−r_∆_t_

_u − d u − d_

1 _− q_˜= _u − d −_ (_u − e−r_∆_t_) = _e−r_∆_t −er_∆_td_ \+ _ud_ \= _e−r_∆_t_(1 _− q_)_d u − d u − d_

_⇒ V<sub>n−</sub>_<sub>1</sub>(_k_) = <sup>h</sup>_qV_˜ _<sub>n</sub>_(_k_ \+ 1) + (1 _− q_˜)_V<sub>n</sub>_ (_k −_ 1)<sup>+i</sup>_._

In short, the expectation does not have to be discounted since _<sub>Vn−</sub>_<sub>1</sub>(_<sub>k</sub>_) = _<sup>Ln</sup><sub>S</sub><sup>−</sup><sub>n−</sub>_<sup>1(</sup><sub>1</sub>_<sup>k</sup>_<sup>)</sup>. That is, _<sub>S</sub>_, whose drift is _<sub>r</sub>_, acts as a numeraire for _<sub>V</sub>_ .

#### Solution 5.7

1.  It is the solution of the arithmetic Brownian motion without drift

_R_(_t_) = _R_(0) + _σW_(_t_)_._

1.  Define the following first hitting time

_τ_ \= inf _{t ≥_ 0 : _R_(_t_) = _H},_

that is,

_._

The probability that the derivative pays $1 is therefore

Q(_τ < T,R_(_T_) _< K_)_,_

or,

Q_τ < T,W_(_T_) _< K − R_(0)_._

_σ_

Using the reflection principle, we obtain

_K_

Q

_T,W_

_τ<_

(

_T_

)

_<_

_K_

_−_

_R_

(0)

_σ_

\=

Q

_W_

(

_T_

)

_\>_

2

_H_

_−_

_R_

(0)

_σ_

_−_

_K_

_−_

_R_

(0)

_σ_

\=

Q

_W_

(

_T_

)

_\>_

2

_H_

_−_

_R_

(0)

_−_

_σ_

\=

Q

_ε>_

2

_H_

_−_

_R_

(0)

_−_

_K_

_√_

_,_

_σ T_

where _<sub>ε</sub>_ is the standard normal variable. Thus, the probability is Φ(_<sub>z</sub>_) with

\= _R_(0) +_√K −_ 2_H._

_z_

_σ T_

(c) The initial value of the derivative is then

_e−rT_ Φ(_z_)_._

#### Solution 5.8

1.  If _<sub>W</sub>_(_<sub>T</sub>_) _<sub>\> y</sub>_ then, by the intermediate value theorem, the Brownian motion will have crossed the level _<sub>y</sub>_ before _<sub>T</sub>_. Thus

P(_θ < T,W_(_T_) _\> y_) = P(_W_(_T_) _\> y_) = Φ_−~~√~~<sup>y</sup> ._

_T_

1.  The reflection principle yields that

P(_θ < T,W_(_T_) _< y_) = P(_W_(_T_) _\> y_) = Φ_−~~√~~<sup>y</sup> ._

_T_

1.  Combining the two preceding results,

P(_θ < T_) = P(_θ < T,W_(_T_) _< y_) + P(_θ < T,W_(_T_) _\> y_)

\= 2Φ_−~~√~~y ._

_T_

1.  The derivative is worth

_g_ \= _e<sup>−rT</sup>_ P(max_W_(_t_) _< y_) = _e<sup>−rT</sup>_ P(_θ > T_) = _e<sup>−rT</sup>_ 1 _−_ 2Φ_−~~√~~<sup>y</sup> <sub>.</sub>_

_T_

#### Solution 5.9

1.  By definition, we get

_c<sub>Asian</sub>_(_T,T,M_(_T_)) _− p<sub>Asian</sub>_(_T,T,M_(_T_)) = \[_S_(_T_) _− M_(_T_)\]<sup>\+</sup> _−_ \[_M_(_T_) _− S_(_T_)\]<sup>\+</sup> \= _S_(_T_) _− M_(_T_)_._

1.  Taking expectations under the EMM and discounting at the risk-free rate, we obtain

_c<sub>Asian</sub>_(0_,T,M_(_T_)) _− p<sub>Asian</sub>_(0_,T,M_(_T_)) = E<sup>Q</sup> \[_S_(_T_) _− M_(_T_)\]_e<sup>−rT</sup> ._

Which yields

_c<sub>Asian</sub>_(0_,T,M_(_T_)) _− p<sub>Asian</sub>_(0_,T,M_(_T_)) = _S_(0) _−_ E<sup>Q</sup> \[_M_(_T_)\]_e<sup>−rT</sup> ._ Using Fubini’s theorem, we obtain

EQ \[_M_(_T_)\] = 1 Z _T_ EQ (_S_(_u_)) d_u_ \= 1 Z _T S_(0)_eru_ d_u_ \= _S_(0) _erT −_ 1_._

_T_ <sub>0</sub> _T_ <sub>0</sub> _rT_

Hence

_cAsian_(0_,T,M_(_T_)) _− pAsian_(0_,T,M_(_T_)) = _S_(0) _− S_(0) 1 _− e−rT . rT_

1.  The put-call parity at time _<sub>t</sub>_ is written as

_c<sub>Asian</sub>_(_t,T,M_(_T_)) _− p<sub>Asian</sub>_(_t,T,M__._

The portion of the average up to time _<sub>t</sub>_ is non-stochastic. Hence

"Z _t_ Z _T_ \# EQ_t_EQ_tS_(_u_)d_u_

_t_

\= 1 Z _t S_(_u_)d_u_ \+ 1 Z _T_ EQ_t_ \[_S_(_u_)\] d_u._

_T_ 0 _T t_

Expanding that expression yields the desired result.

#### Solution 5.10

1.  At time _<sub>T</sub>_

_A_(_T_) = (_x_(_T_) _− y_(_T_))<sup>\+</sup> _≥ x_(_T_) _− y_(_T_) = _B_(_T_)_._ Hence, in the AoA, it must be that for any date _<sub>t ≤ T</sub>_

_A_(_t_) _≥ B_(_t_)_._

1.  The value of the American exchange option is always greater than its intrinsic value. Thus, the American exchange option should never be exercised before maturity. Its value is the same as that of the European exchange option.

#### Solution 5.11

1.  The process _<sub>W</sub>_(_<sub>t</sub>_) is defined as

(_t_) = p_Z<sup>b</sup>_(_t_) _−_ p_ρZ<sup>a</sup>_(_t_) _._

_W_

1 _− ρ_<sup>2</sup> 1 _− ρ_<sup>2</sup>

Since it is the linear combination of Brownian motions, it is normally distributed with zero mean and it has independent increments. Furthermore

V_arZ<sup>b</sup>_(_t_) _ρ_2V_ar_(_Za_(_t_)) 2_ρ_C_ov Zb_(_t_)_,Za_(_t_)

V_ar_(_W_(_t_)) = 1 _− ρ_2 + 1 _− ρ_2 _−_ 1 _− ρ_2

\= 1 _−t ρ_2 + 1_ρ−_2_tρ_2 _−_ 12_−ρ_2_ρt_2

\= _t._

1.  From the martingale property, the rainbow option is worth

 " " ! # #

_e−rT_ EQ _B_(0)exp _rT_ \+ _σbZb_(_T_) 1_A_(_T_)_≥K ._

Using the decomposition of _<sub>Z</sub><sup>b</sup>_(_<sub>T</sub>_), we obtain

_B_(0)E _σb ρZa_(_T_) + q1 _− ρ_2_W_(_T_)#1_A_(_T_)_≥K_#_._

The independence between _<sub>W</sub>_ and _<sub>Z</sub><sup>a</sup>_ yields

<sup>\#</sup> _B_(0)E _bρZ<sup>a</sup> <sub>K</sub> ×_ E_._

The second expectation can be written as

 " # E _T ._

Which yields

" _B_(0)E<sup>Q</sup>_σ<sub>b</sub>ρZ<sup>a</sup>._

The event _<sub>A</sub>_(_<sub>T</sub>_) _≥ <sub>K</sub>_ is equivalent in law to

! := _−d_<sub>2</sub> (_A_(0))_._

_σ T A_

_ε_

_≥_

1

_a_

_√_

ln

_K_

(0)

_−_

_r_

_−_

_σ_

2

_a_

2

!

_T_

Hence the premium for the rainbow option is

 2 2 !

_B_  _Tε ϕ_(_ε_) d_ε._

The change of variable _<sub>Y</sub>_ \= _<sub>ε − σb</sub>ρ<sup>√</sup><sub>T</sub>_ yields

|     |     |     |
| --- | --- | --- |
| with |     | _B_(0)Φ(_x_)_,_ |
| _x_ | \=  | _√_<br><br>(<br><br>_d_<sub>2</sub> _A_(0)) + _σ<sub>b</sub>ρ T,_ |

_T √_

_x_ \= _K <sup>√</sup>_ 2 + _σ<sub>b</sub>ρ T._

_σ<sub>a</sub> T_

#### Solution 5.12

1.  Since the Russian option is a perpetual derivative, its value _<sub>g</sub>_ verifies the following ODE in the BMS framework

_._

1.  Since _<sub>X</sub>_ \= _<sub>S/M</sub>_, then

 _._

Hence

_._

1.  Since _g_ (_X_) = _aX<sup>λ</sup>_<sup>1</sup> \+ _bX<sup>λ</sup>_<sup>2</sup>, then

_,_

_∂_2_g_<sup>2</sup> _λ_1_−_2 + _bλ_2 (_λ_2 _−_ 1)_Xλ_2_−_2_._

\= _λ_1 (_λ_1 _−_ 1)_aX_

_∂X_

Plugging these two partial derivatives into the left hand-side of the ODE, we get, after simplifications

_λ_1 " 2 _σ_2 ! # _aX σ_2 _λ_21 + _λ_1 _r − y −_ 2 _− r_

_<sup>λ</sup>_2 " 2 _σ_2 ! #

+_bX σ_2 _λ_2<sub>2</sub> \+ _λ_2 _r − y −_ 2 _− r ._

Since _<sub>λ</sub>_<sub>1</sub> and _<sub>λ</sub>_<sub>2</sub> are the roots of the quadratic equation

_σ_22 _x_2 + _x_ _r − y − σ_22 ! _− r_ \= 0_,_

then the two terms in brackets are nil, and the left hand-side of the ODE is equal to zero. Hence _g_ (_<sub>X</sub>_) = _<sub>aX</sub><sup>λ</sup>_<sup>1</sup> \+ _<sub>bX</sub><sup>λ</sup>_<sup>2</sup> is indeed the generic solution.

1.  Expanding the two boundary conditions, we get

<sup>(</sup> _aX∗λ_<sub>1</sub> \+ _bX∗λ_<sub>2</sub> \= 1_, λ_<sub>1</sub>_a_ \+ _λ_<sub>2</sub>_b_ \= _a_ \+ _b._

The solution to that system is

_a_ _, b_ _._

1.  Hence the value of the Russian option is

_g_ _Xλ_1

_Xλ_2_,_

which yields, after simplifications

_g_ _._

The optimal exercise policy is obtained with the first order condition

_X._

**Chapter 6**

**Numerical methods**

The value of a derivative is the solution to a PDE which, in the vast majority of situations, has no analytical solution–either because the model is too sophisticated or because the derivative is too complex. In the first section, we present an approach that consists in discretizing the PDE to obtain a numerical pricing algorithm. That approach, referred to as finite differences, proposes several different schemes, depending on the way the Greek parameters appearing in the PDE are discretized. Finite difference methods are extensively used in physics. Their introduction in Finance can be traced back to Brennan and Schwartz (1978). Hull and White (1990b) present a general application of these methods to the pricing of derivatives. Hull and White (1990a) show to adapt that approach to interest rate derivatives. A good survey on finite differences techniques can be found in Wilmott (2000). Finite difference methods can be adapted to a wide variety of UA price dynamics. In addition, they are well suited to price American options. However, they become difficult to implement as the number of state variables increases–the so-called ”curse of dimensionality”.

In the second section we present another numerical approach, which consists in simulating paths for the price of the UA. Monte Carlo simulation techniques were introduced in Finance by Boyle (1977). As we will show, that approach is flexible, too, as it is easy to generate Brownian shocks as well as nonGaussian innovations provided their law is known explicitly. That approach does not suffer from the curse of dimensionality since simulating several state variables is conceptually straightforward and only requires to properly handle the correlation structure among these variables. However, evaluating American options using Monte Carlo simulations is challenging, but not impossible. Another limitation of that approach is the slow convergence, although several techniques address that issue. A much more comprehensive review of Monte Carlo simulation methods can be found in Glasserman (2004).

In the last section, we briefly discuss the pros and cons of the two numerical approaches.

**6.1 Finite differences**

#### 6.1.1 Explicit method

The Explicit Finite Differences Method (EFDM) is by design the simplest scheme among the different finite differences methods. Consider the discretization of time and space leading to a grid made of meshes or

159

nodes. The passage of time is represented in the _<sub>x</sub>_\-axis while the evolution of the UA price is represented in the _<sub>y</sub>_\-axis. Let _<sub>δt</sub>_ and _<sub>δS</sub>_ denote the constant time step and space step, respectively. Figure 6.1 shows how the pricing grid looks like.

D_t_

Figure 6.1: The asset and time steps in the pricing grid.

Recall that in continuous time the application of Itˆo’s lemma and the AoA principle lead to the following

PDE for the value _<sub>g</sub>_ of a derivative written on an UA whose price is driven by a GBM

_._

More generally, in a one-dimensional model with non constant drift and volatility functions, the PDE for _g_ can be written as

_,_ where _<sub>a</sub>_(_<sub>.</sub>_) is related to the volatility function (note that we included the 1_<sub>/</sub>_2 coefficient), _<sub>b</sub>_(_<sub>.</sub>_) is the drift function under the EMM, and _<sub>c</sub>_(_<sub>.</sub>_) must be the negative of the risk-free rate by AoA. Note that the three functions _<sub>a</sub>_(_<sub>.</sub>_), _<sub>b</sub>_(_<sub>.</sub>_) and _<sub>c</sub>_(_<sub>.</sub>_) are determined by the assumptions of the pricing model. In what follows they will be considered as given. A finite differences scheme consists in specifying a way to discretize the Greeks associated to these three functions in the PDE, namely the theta, the gamma, and the delta.

##### Approximation of Greeks

Let _<sub>Ns</sub>_ \+ 1 and _<sub>Nt</sub>_ \+ 1 denote the number of vertical and horizontal nodes in the pricing grid. The space position _<sub>j</sub>_ is numbered from bottom to top, that is, we assume that _<sub>S</sub>_ \= 0 at _<sub>j</sub>_ \= 0 and, for 0 _<sub>≤ j ≤ Ns</sub>_ , _S_ \= _<sub>jδS</sub>_. Note that the space discretization requires that we truncate the distribution of the UA price at some upper boundary. In practice, it can useful to set that boundary (and therefore the value of _<sub>Ns</sub>_) in terms of multiples of strike price to adequately capture the convexity in the option payoff. The time position _n_ is numbered from maturity untill initial date (this is to be consistent with the backward resolution of the algorithm). Hence node _<sub>n</sub>_ \= 0 corresponds to date _<sub>T</sub>_, and, for 0 _<sub>≤ n ≤ Nt</sub>_, node _<sub>n</sub>_ corresponds to date _<sub>T</sub> − <sub>nδt</sub>_. At any node (_<sub>j,n</sub>_) the value of the derivative is denoted by _<sub>gj</sub><sup>n</sup>_.

One possible way to proxy for theta is

_n_+1 _g ≃ . δt_

As far as delta is concerned, the central difference approximation is

∆_g ≃ gjn_+12_−δSgjn−_1 _,_

as shown by Figure 6.2.

Figure 6.2: Delta and theta in the pricing grid. Similarly, gamma can be proxied by (as in the CRR tree)

Γ_<sub>g</sub> ≃ gjn_+1 (∆_S_ 2 _gjn−_1 _._

)

##### Pricing algorithm

Plugging the three Greek parameters proxies into the PDE, we obtain

_gj<sup>n</sup> −δtgjn_+1 + _gj<sup>n</sup>_+1 (_δS_)<sub>2</sub> _gj<sup>n</sup>−_1 _<sub>aj</sub>n_ \+ _gj<sup>n</sup>_+12_−<sub>δS</sub>gj<sup>n</sup>−_1 _<sub>b</sub>n<sub>j</sub>_ \+ _<sub>gj</sub>n<sub>c</sub>n<sub>j</sub>_ \= 0_<sub>,</sub>_

where _<sub>a</sub><sup>n</sup><sub>j</sub>_ , _<sub>b</sub><sup>n</sup><sub>j</sub>_ and _<sub>c</sub><sup>n</sup><sub>j</sub>_ are the values of the functions _<sub>a</sub>_(_<sub>.</sub>_), _<sub>b</sub>_(_<sub>.</sub>_) and _<sub>c</sub>_(_<sub>.</sub>_) evaluated at node (_<sub>j,n</sub>_).

Setting

_v_1 = (_δSδt_)2 _, v_2 = _<sub>δS</sub>δt ,_

|     |     |     |     |
| --- | --- | --- | --- |
| and |     |     |     |
|     | _An<sub>j</sub>_ | \=  | 1<br><br>_v_1_anj −_ 2_v_2_bnj ,_ |
|     | _Bjn_ | \=  | _−_2_v_1_anj_ \+ _δtcnj ,_ |

_Cjn_ \= _v_1_anj_ \+ _v_2_bnj ,_

we get

_gjn_+1 = _Anj gjn−_1 + 1 + _Bjngjn_ \+ _Cjngjn_+1_._ (6.1)

That equation relates the time-_<sub>n</sub>_ \+ 1 value of the derivative with three of its values on the next time step (time _<sub>n</sub>_). Such a pricing algorithm is therefore analogous to that of a trinomial tree. It can be solved using backward induction. Knowing the terminal value of the derivative (i.e., at date _<sub>T</sub>_ \= _<sub>Nt</sub>δt_, all _<sub>gj</sub>_<sup>0</sup> are known), The entire pricing grid can be filled by repeated application of equation (6.1), provided boundary conditions are specified (cf. Figure 6.3).

Figure 6.3: Valuation in the EFDM.

Note that the sum of the coefficients is

_Anj_ \+ 1 + _Bjn_ + _Cjn_ \= 1 + _δtcnj ,_

which is 1 minus the risk-free rate applied to one period. That is, the weights _<sub>A</sub><sup>n</sup><sub>j</sub>_ , 1 + _<sub>Bj</sub><sup>n</sup>_ and _<sub>Cj</sub><sup>n</sup>_ add up to the discount factor. Note also that they are not guaranteed to lie between 0 and 1. Hence the weights are not probabilities. Equation (6.1) thus represents a slight distortion of the martingale property. The time-_<sub>n</sub>_+1 value of the derivative is the average of three future values. However, that average is not exactly the risk-neutral expectation of the future value.

##### Boundary conditions

The recursive algorithm can be completely solved if boundary conditions are set, that is, specific values are assigned (i) upon maturity (right boundary of the grid), (ii) when _<sub>S</sub>_ \= 0 (bottom boundary of the grid), and (iii) when _<sub>S</sub>_ \= _<sub>Ns</sub>δS_ (top boundary of the grid). Terminal conditions are simply

_g<sub>j</sub>_<sup>0</sup> \= terminal payoff when _<sub>S</sub>_ \= _<sub>jδS.</sub>_

Regarding the space dimension, boundary conditions for the European call are

_g_<sub>0</sub>_<sup>n</sup>_ \= 0_,_

_<sup>g</sup><sub>N</sub>n<sub>s</sub>_ \= _<sup>N</sup>sδSe−ynδt − Ke−rnδt,_

while those for the European put are

_<sup>g</sup>_<sub>0</sub>_n_ \= _Ke−rnδt, gNns_ \= 0_._

Alternatively, for the deep ITM/OTM region, the boundary condition can simply reflect the fact that the gamma approaches zero, i.e. the value of the option is almost linear in _<sub>S</sub>_. Which yields

_gNns_ \= 2_gNns−_1 _− gNns−_2

and, if the grid starts at some low value _<sub>S</sub>_<sub>min</sub> \= _<sub>j</sub>_<sub>0</sub>_<sub>δS ></sub>_ 0,

_gjn_0 = 2_gjn_0+1 _− gjn_0+2_._

Once those boundary conditions are defined, the EFDM is an _explicit_ pricing scheme in the sense that the value of the derivative can be calculated at any node in the grid from the mere application of the recursive algorithm. Note, in particular, that the EFDM can be readily applied to evaluating American options. As with trees, the only adjustment in the algorithm consists in systematically taking the maximum between the exercise value and the continuation value given by equation (6.1). Indeed, as we discussed earlier, equation (6.1) yields an acceptable proxy for the continuation value since it is closely related to (yet somewhat different from) the discounted conditional expectation of the derivative future value.

The major drawback of the EFDM is its instability. The grid must be constructed to ensure that the coefficients _<sub>A</sub><sup>n</sup><sub>j</sub>_ , 1 + _<sub>Bj</sub><sup>n</sup>_ and _<sub>Cj</sub><sup>n</sup>_ remain between 0 and 1. If these constraints are not satisfied, this may cause problems near the space boundaries where the sum of the coefficients is not guaranteed to sum up to 1 + _<sub>δtc</sub><sup>n</sup><sub>j</sub>_ . For instance, one negative weight could locally generate a negative value for the derivative. Because the algorithm is explicit, that pricing anomaly will quickly propagate throughout the grid (i.e. the recursive valuation formula (6.1) will amplify, instead of absorbing, the pricing anomaly thereby contaminating the rest of the grid). These constraints imply in particular that

1 + _δtc<sup>n</sup><sub>j</sub>_

_v_1 _≤_ 2_anj ,_

_v_2 2_anj_

_≤_ _. v_1 _bnj_

The first inequality requires that _<sub>δt</sub>_ be small relative to (_<sub>δS</sub>_)<sup>2</sup>, i.e. the grid should have a horizontal, rectangular shape. Put differently, for a given space discretization, time discretization should be sufficiently fine to achieve stability. The second inequality requires that _<sub>v</sub>_<sub>2</sub>_<sub>/v</sub>_<sub>1</sub> \= _<sub>δS</sub>_ be sufficiently small, all else equal. Put together, these constraints call for a fine space discretization and an even finer time discretization, which of course translates into a large pricing grid and therefore increases computational time.

The good news about the EFDM instability issue is that it is usually easily detected. If pricing anomalies spread across the grid, the current derivative price will be absurd. In any case, it is worth checking the values of _<sub>g</sub>_<sub>0</sub>_<sup>Nt</sup>_ and _<sub>gN</sub><sup>N</sup><sub>s</sub><sup>t</sup>_ because the current derivative price _<sub>gj</sub><sup>n</sup>_ with _<sub>jδS</sub>_ \= _<sub>S</sub>_ could look reasonable and could nevertheless be slightly contaminated by anomalies in the corners of the grid.

**Richardson extrapolation** It can be shown that the magnitude of the error associated with the EFDM is of the orders _<sub>δt</sub>_ and (_<sub>δS</sub>_)<sup>2</sup>. In other words, let _<sub>g</sub>_<sub>1</sub> and _<sub>g</sub>_<sub>2</sub> denote two EFDM estimates of the “true” derivative value _<sub>g</sub>_ that are obtained with two different grids using time and space steps _<sub>δt</sub>_<sub>1</sub> and _<sub>δS</sub>_<sub>1</sub> on one hand, and _<sub>δt</sub>_<sub>2</sub> and _<sub>δS</sub>_<sub>2</sub> on the other.

Then,

 _g,_

 _g,_

where _<sub>ai</sub>_ and _<sub>bi</sub>_, _<sub>i</sub>_ \= 1_<sub>,</sub>_2, are coefficients that should be similar, i.e. _<sub>a</sub>_<sub>1</sub> _≃ <sub>b</sub>_<sub>1</sub> and _<sub>a</sub>_<sub>2</sub> _≃ <sub>b</sub>_<sub>2</sub>.

Assuming the coefficients are exactly the same, then we can write a linear combination of the two estimates to eliminate the term in _<sub>a</sub>_<sub>2</sub>, which yields

(_δS_(_δS_2)2 _g_)1 _−−_ (_δS_1)2 _g_2 = _g_ \+ _a_1_δt_1 (_δS_2)22_− a_(1_δS_∆1_t_)22(_δS_1)2 + _O_(_δt_)2 _,_(∆_S_)3_._ 2 _δS_1)2 (_δS_2) _−_

2 (

With the judicious choice

(_δSδt_<sub>1</sub>1)<sup>2</sup> \= (_δSδt_<sub>2</sub>2)<sub>2</sub> _<sub>,</sub>_

the former equality simplifies into

(_δS_2)2 _g_1 _−_ (_δS_1)2 _g_2 = _g_ \+ _O_(_δt_)2 _,_(_δS_)3_._

(_δS_<sub>2</sub>)2 _−_ (_δS_1)2

That is, the ratio on the left-hand side provides a more accurate estimate of _<sub>g</sub>_ since the magnitude of the error is reduced to the orders of (_<sub>δt</sub>_)<sup>2</sup> and (_<sub>δS</sub>_)<sup>3</sup>.

#### 6.1.2 Implicit methods

To address the instability issue related to the EFDM, one can resort to an implicit scheme. There are different ways to construct such a scheme, leading to a family of Implicit Finite Differences Methods (IFDM). Their common feature is that the pricing algorithm relates the value of the derivative to values in the _preceding_ time step of the grid. In this section we present two among the most popular methods: The fully IFDM and the Crank-Nicolson scheme.

Let us return to the EFDM algorithm where the delta and the gamma are now evaluated at date _<sub>n</sub>_+1

_gjn −δtgjn_+1 + _gjn_+1+1 _<sup>−</sup>_ 2_δSgjn_+12 + _gjn−_+11 _a<sub>n</sub>j_ <sub>+1</sub> \+ _gjn_+1+12_−δSgjn−_+11 _b<sub>n</sub>j_ <sub>+1</sub> \+ _gj<sub>n</sub>_<sub>+1</sub>_c<sub>n</sub>j_ <sub>+1</sub> \= 0_._

( )

That equation can be simplified as

|     |     |
| --- | --- |
| _gjn_ \= _αjn_+1_gjn−_+11 + 1 + _βjn_+1_gjn_+1 + _γjn_+1_gjn_+1+1_,_ with | (6.2) |

_αjn_+1 = _−v_<sub>1</sub>_an<sub>j</sub>_ +1 + _v_<sub>2</sub>_bn<sub>j</sub>_ +1_,_

_βjn_+1

_γjn_+1

and _<sub>v</sub>_<sub>1</sub> and _<sub>v</sub>_<sub>2</sub> keep their same definition.

|     |     |
| --- | --- |
| \=  | 2_v_1_anj_ +1 _− δtcnj_ +1_,_ |
| \=  | 1<br><br>_−v_1_anj_ +1 _− v_2_bnj_ +1_,_ |

2

Equation (6.2) relates the value _<sub>gj</sub><sup>n</sup>_ with three values at the preceding time node, as illustrated below. It is referred to as the fully IFDM. By construction, an implicit scheme will eliminate the instability issue. This is because the set of derivative prices at one point in time is now much more intertwined by the system of equations connecting them. Should an erroneous price appear, the anomaly will no longer spread out due to backward induction. On the contrary, since every price _<sub>gj</sub><sup>n</sup>_<sup>+1</sup> is involved in three different equations, the implicit scheme entails greater discipline on price consistency and, as a matter of fact, prevents pricing anomalies from propagating throughout the grid (cf. Figure 6.4).

Applying equation (6.2) for all _<sub>j</sub>_, _<sub>j</sub>_ \= 1_<sub>,...Ns</sub> −_1 and adding boundary conditions at _<sub>j</sub>_ \= 0 and _<sub>j</sub>_ \= _<sub>Ns</sub>_, we obtain a system of _<sub>Ns</sub>−_1 linear equations and _<sub>Ns</sub>−_1 unknowns for every _<sub>n</sub>_. Thus, the pricing algorithm is still solved backwards, but it no longer relies on backward induction. Rather, a system of equations must be solved at every time step, which typically involves the inversion of a matrix. Such a resolution method can be time-consuming. However, we will present an alternative, faster way to solve the pricing algorithm.

#### 6.1.3 Crank-Nicolson algorithm

##### Definition

The Crank-Nicolson scheme consists in combining the EFDM with the fully IFDM. Specifically, the EFDM scheme is

_gjn_+1 = _Anj gjn−_1 + 1 + _Bjngjn_ \+ _Cjngjn_+1_,_

Figure 6.4: Valuation in the IFDM.

while the fully IFDM scheme is

_gjn_ \= _αjn_+1_gjn−_+11 + 1 + _βjn_+1_gjn_+1 + _γjn_+1_gjn_+1+1_._

Adding the two equations together, we obtain

_gjn_+1 + _gjn_ \= _Anj gjn−_1 + 1 + _Bjngjn_ \+ _Cjngjn_+1

+_αjn_+1_gjn−_+11 + 1 + _βjn_+1_gjn_+1 + _γjn_+1_gjn_+1+1_._

Define

_hnj_ \= _−Anj gjn−_1 _− Bjngjn − Cjngjn_+1_._

Note that computing _<sub>h</sub><sup>n</sup><sub>j</sub>_ is straightforward as it only involves contemporaneous terms at date _<sub>n</sub>_. Inserting _h<sup>n</sup><sub>j</sub>_ into the pricing scheme yields

_hnj_ \= _αjn_+1_gjn−_+11 + _βjn_+1_gjn_+1 + _γjn_+1_gjn_+1+1_,_

which corresponds to an IFDM. In other words, the Crank-Nicolson algorithm is similar to the fully IFDM except that the left-hand side of the equation is a recombination of time-_<sub>n</sub>_ terms that incorporates the pricing relation from the EFDM. Recall that the EFDM captures the martingale property of asset prices, whereas no implicit scheme does. It is therefore hoped that the Crank-Nicolson algorithm offers the stability of an implicit method with a faster convergence to the true derivative price. Numerical experiments reported below will show that it is indeed the case.

##### Resolution

As mentioned earlier, an implicit scheme (including the Crank-Nicolson algorithm) can be solved by inverting a matrix at every time step. A faster resolution method is the Successive Over-Relaxation (SOR) method. Recall an implicit scheme can be written as

_<sup>α</sup><sub>j</sub>n_+1_<sup>g</sup><sub>j</sub>n<sub>−</sub>_+1<sub>1</sub> \+ _<sup>β</sup><sub>j</sub>n_+1_<sup>g</sup><sub>j</sub>n_+1 + _<sup>γ</sup><sub>j</sub>n_+1_<sup>g</sup><sub>j</sub>n_<sub>+1</sub>+1 = _hn<sub>j</sub> ,j_ \= 1_,...,Ns −_ 1_,_

where the _<sub>h</sub><sup>n</sup><sub>j</sub>_ terms are known at date _<sub>n</sub>_. The SOR method proceeds by iterations. Let _<sub>gj</sub>_ (superscript _<sub>n</sub>_+1 is dropped for convenient notations)

(_u_)

denote the value of _<sub>gj</sub><sup>n</sup>_<sup>+1</sup> obtained after _<sub>u</sub>_ iterations. Using the Gauss-Seidel iterative procedure, _<sub>gsx</sub>_<sup>(</sup>_<sup>u</sup>_<sup>)</sup> is calculated as

|     |     |     |
| --- | --- | --- |
| (_u_)<br><br>_g<sub>j</sub>_ | \=  | 1 _n_+1 _nj − αjn_+1_gj_(_u−_)1 _− γjn_+1_gj_(_u_+1_−_1)<br><br>_h β<sub>j</sub>_ |
|     | \=  | (_u−_1)<br><br>_gj_ \+ _n_1+1 _hnj − αjn_+1_gj_(_u−_)1 _− βjn_+1_gj_(_u−_1) _− γjn_+1_gj_(_u_+1_−_1)_,_ |

_β<sub>j</sub>_

where the second term of the last equation represents the update on _<sub>gj</sub><sup>n</sup>_<sup>+1</sup> during the _<sub>u</sub><sup>th</sup>_ iteration. Note that this iterative procedure for _<sub>gj</sub>_ involves _<sub>gj−</sub>_<sub>1</sub>, that is, a term calculated previously but during the

(_u_) (_u_)

same iteration.

Since the convergence of iterations is monotonic, we can accelerate it by multiplying the updating term by a constant _<sub>ω</sub>_, typically between 1 and 2. Which yields

(_u_) = (_u−_1) + _ω_ _n − αjn_+1_gj_(_u−_)1 _− βjn_+1_gj_(_u−_1) _− γjn_+1_gj_(_u_+1_−_1)_. gj gj n_+1 _hj β<sub>j</sub>_

To initialize the iterations, a simple starting value is

_gj_(0) = _gjn,_

i.e., the value of the derivative on the same space node obtained on the preceding time step (backward resolution).

Finally, iterations must be stopped once a given criterion for accuracy is satisfied. One possibility is to select a floor on the total update on the derivative prices, that is, end up at iteration _<sub>u</sub>_ when it verifies for the first time that

v

u<sup>u</sup>_N_X_s−_1 (_u_) (_u−_1)<sub>2</sub>

ut _gj − gj < ϵ,_

_j_\=1

where _<sub>ϵ</sub>_ is an arbitrarily small tolerance level.

One major advantage of the iterative procedure is that it allows for an easy adaptation of implicit schemes (including the Crank-Nicolson algorithm) to the pricing of American options.

Recall that the proper evaluation of American options requires the systematic comparison between the exercise value and the continuation value. The continuation value is the discounted conditional expectation of the derivative future value, obtained from the application of the martingale property. One issue with implicit schemes is that the martingale property does not explicitly appear in the pricing algorithm. Hence the _<sub>gj</sub><sup>n</sup>_ obtained from matrix inversion may not accurately represent continuation values, thereby creating a potential bias in the evaluation of American options.

It turns out that applying the systematic comparison between exercise and continuation values during the iteration procedure greatly reduces this bias. Hence, American options can be evaluated using the following scheme

(_u_)

_gj_ \= max"_gj_(_u−_1) + _nω_+1 _hjn − αjn_+1_gj_(_u−_)1 _− βjn_+1_gj_(_u−_1) _− γjn_+1_gj_(_u_+1_−_1)_,exj_#_,_

_β<sub>j</sub>_

where _<sub>exj</sub>_ is the exercise value of the derivative when the UA price is at level _<sub>j</sub>_. Such adjusted pricing scheme is referred to as the PSOR method (Projected Successive Over-Relaxation).

#### 6.1.4 Numerical example

We apply the numerical schemes examined above to evaluate an option. Consider the European put written on an UA without any dividend, with strike price 50 and 1-year maturity. The risk-free rate is 10% and the UA return volatility is 40%. We investigate three levels of moneyness, whether the current UA price is 40, 50 or 60. Analytical BMS solutions are

_p_(0_<sub>,</sub>_1_<sub>,</sub>_50_|<sub>S</sub>_ \= 40) = 9_<sub>.</sub>_6901_<sub>,</sub> p_(0_<sub>,</sub>_1_<sub>,</sub>_50_|<sub>S</sub>_ \= 50) = 5_<sub>.</sub>_4011_<sub>,</sub> p_(0_<sub>,</sub>_1_<sub>,</sub>_50_|<sub>S</sub>_ \= 60) = 2_<sub>.</sub>_9153_<sub>.</sub>_

We first resort to a simple CRR tree (without initializing the algorithm with the BMS put formula at the former to last date, to properly compare the quality of convergence with finite difference methods). We obtain

##### ~~Number of time steps 100 200 400 800 1,600~~

_p<sub>CRR</sub>_(0_<sub>,</sub>_1_<sub>,</sub>_50_|<sub>S</sub>_ \= 40) 9.6913 9.6834 9.6928 9.6892 9.6899 _p<sub>CRR</sub>_(0_<sub>,</sub>_1_<sub>,</sub>_50_|<sub>S</sub>_ \= 50) 5.3817 5.3914 5.3963 5.3987 5.3999 _p<sub>CRR</sub>_(0_<sub>,</sub>_1_<sub>,</sub>_50_|<sub>S</sub>_ \= 60) 2.9234 2.9176 2.9189 2.9171 2.9151

Regarding finite differences methods, we set _<sub>δS</sub>_ \= 2_<sub>.</sub>_5\. The corresponding number of time steps is such that _<sub>δt × n</sub>_ \= 1_<sub>/</sub>_2\. Results for the EFDM are as follows

~~Number of time steps 100 200 400 800 1,600~~ _p<sub>EFDM</sub>_(0_,_1_,_50_|S_ \= 40) # # 9.6884 9.6881 9.6879 _p<sub>EFDM</sub>_(0_,_1_,_50_|S_ \= 50) # # 5.3997 5.3987 5.3982 _p<sub>EFDM</sub>_(0_,_1_,_50_|S_ \= 60) # # 2.9141 2.9132 2.9128

The symbol # indicates an unstable algorithm yielding an exploding solution. Results for the fully IFDM are as follows

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| ~~Number of time steps~~ | ~~100~~ | ~~200~~ | ~~400~~ | ~~800~~ | ~~1,600~~ |
| _p<sub>IFDM</sub>_(0_,_1_,_50_\|S_ \= 40) | 9.6852 | 9.6865 | 9.6871 | 9.6874 | 9.6876 |
| _p<sub>IFDM</sub>_(0_,_1_,_50_\|S_ \= 50) | 5.3899 | 5.3938 | 5.3958 | 5.3968 | 5.3973 |
| _p<sub>IFDM</sub>_(0_,_1_,_50_\|S_ \= 60) | 2.9055 | 2.9089 | 2.9106 | 2.9115 | 2.9119 |

Results for the Crank-Nicolson algorithm are as follows

Number of time steps 25 50 100 200

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
| _p<sub>CN</sub>_(0_,_1_,_50_\|S_ \= 40) | 9.6878 | 9.6877 | 9.6877 | 9.6877 |
| _p<sub>CN</sub>_(0_,_1_,_50_\|S_ \= 50) | 5.3986 | 5.3978 | 5.3978 | 5.3977 |
| _p<sub>CN</sub>_(0_,_1_,_50_\|S_ \= 60) | 2.9126 | 2.9124 | 2.9124 | 2.9124 |

We note from these numerical experiments that:

1.  As expected, the EFDM is subject to stability issues. It takes a sufficient number of time steps to obtain a plausible result. By contrast, IFDM (including the Crank-Nicolson approach) do not suffer from these issues.
2.  Convergence of the CRR tree solution is oscillatory. As we noted, this can be fixed with the Broadie and Detemple (1996) adjustment. Finite differences methods seem to display monotonic convergence, but oscillations will appear if we examine narrower time steps. Note that the convergence point of the CRR tree is more closely centered on the ”true” price than those of the three finite differences methods. Clearly, the CRR tree appears a much better discretization scheme for the log-normal price dynamics of the BMS world. Finite difference methods will be preferred only for more complex price dynamics that cannot be captured within a binomial or a trinomial tree. 3. Speed of convergence can be measured with the following ratio

_g_ (2_N_) _− g_ (_N_)

_, g_ (4_N_) _− g_ (2_N_)

where _<sub>g</sub>_(_<sub>N</sub>_) stands for the estimate of the derivative value obtained using _<sub>N</sub>_ time steps (recall space step is fixed in our experiments). For the ATM put, the CRR tree, EFDM, and fully IFDM methods exhibit a ratio of about 2. This is referred to as a linear convergence. By contrast, the ratio for the Crank-Nicolson algorithm is about 4, indicating quadratic convergence. This higher speed of convergence explains the relatively low number of time steps required to reach the convergence point.

**6.2 Monte Carlo simulations**

#### 6.2.1 The simulation principle

Simulating a model consists in generating UA price paths to construct discrete (i.e. point by point) distributions of UA future prices. The higher the number of paths, the more accurate the discretized distributions will be. Monte Carlo simulations usually proceed along the following steps:

1.  Determine a discrete time step _<sub>δt</sub>_. Let _<sub>Xt</sub>_ \= _<sub>X</sub>_(_<sub>tδt</sub>_), for _<sub>t</sub>_ \= 0_<sub>,...,N</sub>_ (= _<sub>T/δt</sub>_), be the discretized dynamics of any given process _<sub>X</sub>_.
2.  For every _<sub>δt</sub>_ generate (under the EMM for pricing) a random draw from the innovation driving the UA price. Given _<sub>St</sub>_, compute the next UA price _<sub>St</sub>_<sub>+1</sub> according to the specified price dynamics.
3.  Repeat step 2 to construct a high number (say _<sub>j</sub>_ \= 1_<sub>,...,Ns</sub>_) of UA price paths.
4.  Evaluate the derivative payoff for each path (payoff can be terminal or more complex in the case of a path dependent derivative).
5.  From the martingale property, the current value of the derivative is the average of payoffs discounted at the risk-free rate across the _<sub>Ns</sub>_ paths.

As far as diffusion mo_<sub>√</sub>_dels are concerned, the innovations are realizations of Brownian increments, which are identical in law to _<sub>δtε</sub>_.<sup>1</sup> Consequently, a simulation scheme for the GBM goes as follows

 ! _√_ !

_S<sub>t</sub>_<sub>+1</sub> \= _S<sub>t</sub>_ exp _rδt_ \+ _σ δtε<sub>t</sub> ._

If the goal is to evaluate a European-style derivative, the terminal distribution of the UA price can be readily simulated using

 ! _√_ ! _S_(_T_) = _S_(0)exp _r T_ \+ _σ Tε ._

When the diffusion model driving the UA price does not admit any solution, one must resort to simulating a discretized version of the stochastic differential equation. A simple method is referred to as the Euler discretization scheme.

For example, dynamics commonly used to model interest rates, foreign exchange rates, or commodity convenience yields include the Ornstein-Uhlenbeck process

d_S_(_t_) = _−θS_(_t_)d_t_ \+ _η_ d_W_(_t_)_,_

or the square-root process

d_X_(_t_) = _α_(_β − X_(_t_)) d_t_ \+ _σ_<sup>q</sup>_X_(_t_)d_Z_(_t_)_._

The Euler discretization schemes for these processes are, respectively

_√_

_S<sub>t</sub>_<sub>+1</sub> \= _S<sub>t</sub>_ (1 _− θδt_) + _η δtε<sub>t</sub>,_

_√_

_X<sub>t</sub>_<sub>+1</sub> \= _X<sub>t</sub>_ \+ _α_(_β − X<sub>t</sub>_)_δt_ \+ _σ_<sup>p</sup>_X<sub>t</sub> δtε<sub>t</sub>._

It is also possible to simulate non-normal sources of risk, provided the cdf _<sub>F</sub>_ (_<sub>.</sub>_) of innovations is known explicitly. In this case, a random draw from the specified distribution can be generated using

_F<sup>−</sup>_<sup>1</sup> (_U_)_,_

where _<sub>U</sub>_ is a draw from the uniform law on \[0_<sub>,</sub>_1\].

<sup>1</sup>One efficient way to generate draws from the standard normal distribution is the Box-Muller method: Given _u_<sub>1</sub> and _u_<sub>2</sub> two draws from the uniform law on \[0_,_1\], then the random variables

_√_

_ε_<sub>1</sub> \= _−_2ln_u_<sub>1</sub> cos(2_πu_<sub>2</sub>)_, √_

_ε_<sub>2</sub> \= _−_2ln_u_<sub>1</sub> sin(2_πu_<sub>2</sub>)_,_

are normally distributed with zero mean and unit variance.

#### 6.2.2 Stochastic discounting

If the model accounts for stochastic interest rates, and the instantaneous risk-free rate _<sub>r</sub>_(_<sub>t</sub>_) is among the state variables, then any time-_<sub>T</sub>_ payoff must be discounted with the stochastic discount factor

_T_ !

Z

exp _− r_(_u_)d_u ._

0

In the simulated version of the model, each payoff must be discounted along the path followed by _<sub>r</sub>_(_<sub>t</sub>_).

That is, the time-_<sub>T</sub>_ discount factor for path _<sub>j</sub>_ is

_N−_1 _N−_1 !

Y exp_−rt_(_j_)_δt_ = exp _−_ X _rt_(_j_)_δt ,_

_t_\=0 _t_\=0

where _<sub>N</sub>_ \= _<sub>T/δt</sub>_ is the number of time steps till _<sub>T</sub>_, and _<sub>rt</sub>_<sup>(</sup>_<sup>j</sup>_<sup>)</sup> is the instantaneous risk-free rate at time step _t_ simulated along path _<sub>j</sub>_.

Let _<sub>R</sub>_<sup>(</sup>_<sup>j</sup>_<sup>)</sup> denote the average instantaneous risk-free rate simulated along path _<sub>j</sub>_ (where the average is taken from time 0 to time (_<sub>N</sub> −_ 1)_<sub>δt</sub>_)

_R_(_j_) <sub>\=</sub> 1 _N_X_−_1 _<sub>rt</sub>_(_j_)_<sub>.</sub>_

_N_

_k_\=0

Then the relevant discount factor for any time-_<sub>T</sub>_ payoff is

exp_−R_(_j_)_T._

#### 6.2.3 Correlated underlying assets

The repeated simulation of draws from the normal law (whether through the Box-Muller method or any other approach) yields uncorrelated innovations. Yet, models involving several state variables usually assume a certain correlation structure among them.

Without any loss in generality, consider the model relying on _<sub>Na</sub>_ GBM

_<sup>dSi</sup>_((_t<sup>t</sup>_)) = (_r − <sub>yi</sub>_) d_t_ \+ _σ<sub>i</sub>_ d_W<sub>i</sub>_(_t_)_,i_ \= 1_,...n. S<sub>i</sub>_

Brownian motions are correlated with one another, so that, for all pairs _{<sub>i,j</sub>} ∈_ \[1_<sub>,Na</sub>_\] _×_ \[1_<sub>,Na</sub>_\]

d_W<sub>i</sub>_(_t_) _·_ d_W<sub>i</sub>_(_t_) = _ρ<sub>ij</sub>_ d_t._

The simulation scheme for that model is the following

 ! _√_ !

_Si,t_+1 = _Si,t_ exp _rδt_ \+ _σ<sub>i</sub> δte<sub>i,t</sub> ,_

where innovations must verify

E \[_ei,tej,t_\] = _ρij._

The Cholesky decomposition allows to generate normal draws with the appropriate correlation structure. For each state variable, define (we drop the time dependence for convenient notations)

_i_

_ei_ \= X _αikε_b_k,_

_k_\=1

where CD: the _<sub>ε</sub>_<sub>b</sub>_k_ are _simulated_ (i.e., pseudo-random) standard normal draws which, by construction, are independent from one another.

The variables _<sub>ei</sub>_ are normally distributed with zero mean, since they are linear combinations of normally distributed variables with zero mean. Furthermore, we require that

Var (_<sub>ei</sub>_) = 1_<sub>,</sub>_ E \[_e<sub>i</sub>e<sub>j</sub>_\] = _ρ<sub>ij</sub>,_

which yields

_i_

X _α<sub>ik</sub>_2 = 1_,_

_k_\=1

and, for all _<sub>j < i</sub>_

_j_

X _αikαjk_ \= _ρij._

_k_\=1 To solve for this system, a simple solution is

_e_<sub>1</sub> \= _ε_<sub>1</sub>_, e_2 = _α_21_ε_1 + _α_22_ε_2_,_

where coefficients _<sub>α</sub>_<sub>21</sub> and _<sub>α</sub>_<sub>22</sub> verify

( _α_<sub>21</sub>2 + _α_222 = 1_, α_21 = _ρ_21_._

For three state variables, the algorithm goes on with

_e_3 = _α_31_ε_1 + _α_32_ε_2 + _α_33_ε_3_,_

where coefficients _α_<sub>31</sub>, _α_<sub>32</sub> and _α_<sub>33</sub> verify







and so on and so forth until _<sub>en</sub>_.

_α_312 + _α_322 + _α_332 = 1_, α_31_α_21 + _α_32_α_22 = _ρ_32_, α_31 = _ρ_31_,_

#### 6.2.4 American options

Applying Monte Carlo simulations to the pricing of American options has been challenging for a long time. A major difficulty is that the numerical method goes _forward_ (by constructing US price paths at period after another), while the continuation value of an American option is a conditional expectation that must be calculated by backward induction. In the basic simulation scheme, the future values of the UA price are the ones generated along the same path, and this is clearly not enough to determine the continuation value.

Several adaptations to the simulation algorithm have been introduced: Dynamic programming applied to space partitions (Barraquand and Martineau, 1995), simulated trees (Broadie and Glasserman, 1997), simulated optimal exercise frontier (Ib´an˜ez and Zapatero, 2004). We shall focus on the regression-based approach initially described by Carri\`ere (1996) and further developed by Longstaff and Schwartz (2001), Cl´ement et al. (2002), and Stentoft (2004). That approach proceeds as follows.

The first step consists in simulating _<sub>N</sub>_ paths of the UA price until horizon _<sub>T</sub>_ (the American option maturity date). The vector of derivative values upon maturity <sup>n</sup>_<sub>g</sub>_<sup>(</sup>_<sup>j</sup>_<sup>)</sup>(_<sub>T</sub>_)<sup>o</sup> is computed from the

_j_\=1_,...,Ns_

vector of terminal UA prices <sup>n</sup>_<sub>S</sub>_<sup>(</sup>_<sup>j</sup>_<sup>)</sup>(_<sub>T</sub>_)<sup>o</sup> .

Then the algorithm proceeds backward by taking, for each path, at each time step, the maximum_<sup>j</sup>_<sup>\=1</sup>_<sup>,...,Ns</sup>_ between the exercise value and the continuation value. Exercise value _<sub>g</sub><sup>ex</sup>_ is simply given by

_gt_ \= _St_(_j_) _− K_\+ _,_ for a call, _ex_(_j_)

_gt K − St_(_j_)+ _,_ for a put. _ex_(_j_) = The continuation value is obtained by means of an OLS regression (see the details below).

Once that second step is completed until initial date, the optimal exercise date _<sub>τ</sub>_<sup>(</sup>_<sup>j</sup>_<sup>)</sup> is determined for each path. This date is simply the first time (in chronological order) that the exercise value exceeds the continuation value. Then the value of the American option is the average of discounted payoffs

_g_ \= _N_1_s j_<sup>X</sup>_<sup>N</sup>_\=1_<sup>s</sup> e−rτ_<sup>(</sup>_<sup>j</sup>_<sup>)</sup>_<sup>g</sup><sub>τ</sub>ex_(_j_()_j_)1_<sub>τ</sub>j<sub><N</sub>_ \+ _e−rT g__._

Under very general conditions (see Bergman et al. (1996), for a deeper characterization of these conditions), the continuation value is a monotonic, convex function of the UA price. A fundamental result in algebra states that any such function can be approximated by a series of polynomials formed with basis functions. For every time step _<sub>t</sub>_, the continuation value is therefore proxied by

_M_

E \[_gt_+1 (_St_+1)_|St_ \= _x_\] = X _βu,tϕu_ (_x_)_,_

_u_\=1

where the _<sub>ϕu</sub>_ (_<sub>·</sub>_) are the basis functions (the regressors), _<sub>M</sub>_ is the number of regressors, and the _<sub>βu,t</sub>_ are the coefficients obtained from an OLS regression.

Longstaff and Schwartz (2001) suggest to use Legendre or Laguerre polynomials. They further restrict the regression to the paths where the American option is in the money. Admittedly, the quality of the American option estimate increases with _<sub>M</sub>_ and _<sub>Ns</sub>_, but so does the computing time.

The simplified example below illustrates how the method works. The UA price is currently 100. The simulation of 8 paths over 3 time steps yields the following results

|     |     |     |     |
| --- | --- | --- | --- |
| Path _<sub>t</sub>_ | _t_ | _t_ | _t_ |
| 2 100 | 77  | 70  | 72  |
| 3 100 | 97  | 86  | 163 |
| 4 100 | 122 | 161 | 79  |
| 5 100 | 128 | 103 | 127 |
| 6 100 | 131 | 143 | 139 |
| 7 100 | 103 | 116 | 61  |
| 8 100 | 82  | 62  | 126 |

The goal is to evaluate the ATM American call expiring at date _<sub>t</sub>_<sub>3</sub>. Upon maturity, the call is in the money for paths 3, 5, 6 and 8. We then proceed to the regression at time _<sub>t</sub>_<sub>2</sub>. There are four paths where the call is ITM (4, 5, 6 and 7), which gives us four points for the regression: _<sub>{</sub>_161;0_<sub>}</sub>_, _<sub>{</sub>_103;27_<sup>∗</sup><sub>}</sub>_, _<sub>{</sub>_143;39_<sup>∗</sup><sub>}</sub>_ and _{_116;0_<sub>}</sub>_. The star superscripts indicate that these values should be discounted at the risk-free rate over one period (we omit discounting in this example for clarity of presentation).

Suppose we use the second order polynomial as the regressor, we obtain (all numerical values are rounded at the third decimal)

E\[_g<sub>t</sub>_<sub>3</sub> (_S<sub>t</sub>_<sub>3</sub>)_|S<sub>t</sub>_<sub>2</sub> \= _x_\] := _q_<sub>2</sub> (_x_) = _−_0_._015_x_<sup>2</sup> \+ 3_._857_x −_ 221_._607_._

Consequently, the time-_<sub>t</sub>_<sub>2</sub> continuation values for points where the call is ITM are estimated as follows

_q_<sub>2</sub> (161) = 7_<sub>.</sub>_525_<sub>, q</sub>_<sub>2</sub> (103) = 15_<sub>.</sub>_578_<sub>,</sub> q_<sub>2</sub> (143) = 20_<sub>.</sub>_814_<sub>, q</sub>_<sub>2</sub> (116) = 22_<sub>.</sub>_383_<sub>.</sub>_

Clearly, the estimation is of poor quality as the function is not monotonically increasing with _<sub>S</sub>_. This will no longer be the case as the number of observations (generated by more simulated paths) increases. The American call at time _<sub>t</sub>_<sub>2</sub> is therefore worth

|     |     |
| --- | --- |
| Path _S<sub>t</sub>_<sub>2</sub> | _gt_<sub>2</sub> |
| 1 97 | 0   |
| 2 70 | 0   |
| 3 86 | 0   |
| 4 161 | max (161) _ex_(4) = 61 _q_2 _,gt_2 |
| 5 103 | max_q_2 (103)_,gtex_2 (5) = 15_._578 |
| 6 143 | max (143) _ex_(6) = 43 _q_2 _,gt_2 |
| 7 116 | max_q_2 (116)_,gtex_2 (7) = 22_._383 |
| 8 62 | 0   |

The recursive algorithm moves on to date _<sub>t</sub>_<sub>1</sub>. The new regression is estimated from the paths where the call is ITM (4, 5, 6 and 7). The four observations are: _<sub>{</sub>_122;61_<sup>∗</sup><sub>}</sub>_, _<sub>{</sub>_128;27_<sup>∗∗</sup><sub>}</sub>_, _<sub>{</sub>_131;43_<sup>∗</sup><sub>}</sub>_ and _<sub>{</sub>_103;0_<sub>}</sub>_.

Note the continuation values take all outcomes along the path into account. For path #5 in particular, the non-exercise at time _<sub>t</sub>_<sub>1</sub> leads to the non-exercise at time _<sub>t</sub>_<sub>2</sub>, which leads to the exercise at terminal date _<sub>t</sub>_<sub>3</sub> and a payoff of 27 that must be discounted over two time steps (hence the double star superscript). For path #7, the non-exercise at time _<sub>t</sub>_<sub>1</sub> leads to the non-exercise at time _<sub>t</sub>_<sub>2</sub>, which leads to the call expiring OTM and a payoff of 0. In retrospect, the call should have been exercised at time _<sub>t</sub>_<sub>2</sub> along this path. But the American call holder rationally chose not to as he or she could not anticipate the drop in UA price on the next period.

Using the same set of regressors, we obtain

E\[_g<sub>t</sub>_<sub>2</sub> (_S<sub>t</sub>_<sub>2</sub>)_|S<sub>t</sub>_<sub>1</sub> \= _x_\] := _q_<sub>1</sub> (_x_) = _−_0_._182_x_<sup>2</sup> \+ 43_._692_x −_ 2571_._76_,_

and the time-_<sub>t</sub>_<sub>1</sub> continuation values are

|     |     |
| --- | --- |
| _q_<sub>1</sub> (122) = 53_<sub>.</sub>_817_<sub>,</sub>_ | _q_<sub>1</sub> (128) = 43_<sub>.</sub>_378_<sub>,</sub>_ |
| _q_<sub>1</sub> (131) = 33_<sub>.</sub>_251_<sub>,</sub>_ | _q_<sub>1</sub> (103) = 0_<sub>.</sub>_554_<sub>.</sub>_ |

The American call values at time _<sub>t</sub>_<sub>1</sub> are

|     |     |
| --- | --- |
| Path _S<sub>t</sub>_<sub>1</sub> | _gt_<sub>1</sub> |
| 1 78 | 0   |
| 2 77 | 0   |
| 3 97 | 0   |
| 4 122 | max_q_1 (122)_,gtex_1 (4) = 53_._817 |
| 5 128 | max_q_1 (128)_,gtex_1 (5) = 43_._378 |
| 6 131 | max_q_1 (131)_,gtex_1 (6) = 33_._251 |
| 7 103 | max (103) _ex_(7) = 3 _q_1 _,gt_1 |
| 8 82 | 0   |

The table below reports the optimal exercise dates and associated payoffs for each path

|     |     |     |     |
| --- | --- | --- | --- |
| Path _t_<sub>0</sub> | _t_1 | _t_2 | _t_3 |
| 1<br><br>2<br><br>3 |     |     | 63  |
| 4   |     | 61  |     |
| 5   |     |     | 27  |
| 6   |     | 43  |     |
| 7   | 3   |     |     |
| 8   |     |     | 26  |

Suppose the risk-free rate is 5% per period, the initial value of the American call is

_g_ \= _e−_0_._805_×_3 (63 + 27 + 26) + _e−_0_._805_×_2 (61 + 43) + _e−_80_._05 (3) = 24_._6_._

#### 6.2.5 Convergence improvements

One major drawback for Monte Carlo simulations is that it often takes a high number of paths to obtain an accurate description of the UA return distribution. Thus, the method may require substantial computing time to achieve an acceptable level of pricing precision. That is why several techniques have been developed to accelerate convergence. We shall present two of the most common ones. For a more in depth review of these techniques we refer to Glasserman (2004).

The _control variate_ technique, in its basic version, can in fact be applied to any numerical method (not only Monte Carlo simulations, but also trees or finite differences). Suppose our pricing problem _<sub>g</sub>_ admits no analytical solution, which is why we are resorting to a numerical approach returning the estimate _<sub>g</sub>_<sub>b</sub>. There is, however, a ”closely related” pricing problem for which the explicit solution is _<sub>gc</sub>_. That same numerical approach applied to the explicit pricing problem (or, simply, the control problem) returns the estimate _g_<sub>b</sub>_c_.

Hull and White (1988) introduced the basic version of the control variate technique by assuming that the pricing error on the numerical problem is of similar magnitude to the pricing error made on the control problem. Therefore a better estimate for _<sub>g</sub>_ should be

_g_<sub>b</sub> \+ _g<sub>c</sub> − g_<sub>b</sub>_c._

Intuitively, this price correction relies on an assumption that is all the weaker since the two pricing problems are close in nature. For that reason, Broadie and Glasserman (1998) suggest to use Asian options with geometric averaging as control variates to evaluate Asian options with arithmetic averaging. In the same spirit, Clewlow and Carverhill (1994) show how to improve the convergence of Monte Carlo simulations by using control variates that match Greek parameters of the derivative to evaluate.

The control variate technique can be refined if one assumes that the pricing error on the numerical problem is only a fraction _<sub>α</sub>_ of the control problem (see, e.g., Law and Kelton, 2000). Hence a revised estimate for _<sub>g</sub>_ would be

_g_<sub>b</sub>(_α_) = _g_<sub>b</sub> _− α_(_g_<sub>b</sub>_c − g<sub>c</sub>_)_,_

where _<sub>α</sub>_ is a real number (not necessarily equal to one, as in the basic version of the method).

The goal is to reduce the variance around that estimator. Given that

Var (_g_<sub>b</sub>(_α_)) = Var (_g_<sub>b</sub>) + _α_<sup>2</sup> Var (_g_<sub>b</sub>_c_) _−_ 2_α_Cov (_g,_<sub>b</sub> _g_<sub>b</sub>_c_)_,_

the control variate effectively reduces the variance if and only if

_α_<sup>2</sup> Var (_g_<sub>b</sub>_c_) _<_ 2_α_Cov (_g,_<sub>b</sub> _g_<sub>b</sub>_c_)_._

By simply setting _<sub>α</sub>_ \= _<sub>±</sub>_1 (as in Hull and White, 1988), that condition is met only if

_|_Cov (_g,_b _g_b_c_)_| >_ Var (2 _g_b_c_)_,_

and we see the variance reduction technique is successful only if the control problem estimate is highly correlated with the numerical problem estimate (this is what we meant by two ”closely related” problems).

We can determine the value of _<sub>α</sub>_ that minimizes Var (_<sub>g</sub>_<sub>b</sub>(_<sub>α</sub>_)) from the first order condition

_α∗_ \= Cov (Var (_g,_b_g_b_cg_b)_c_)_._

Hence _<sub>α</sub><sup>∗</sup>_ can be estimated from a simple linear regression.

The first step consists in selecting a good candidate for the control variate. As explained earlier, it must be the pricing problem with an explicit solution that requires the least modifications from the original numerical pricing problem. One can think of pricing the same derivative in a slightly simplified model. Alternatively, it could be a simpler derivative contract evaluated within the same pricing framework.

Once the control variate is identified, the numerical method is applied a big number of times to generate the estimates _<sub>g</sub>_<sub>b</sub> and _<sub>g</sub>_<sub>b</sub>_c_. This is clearly the most time consuming part of the control variate technique. The cost is not too high for Monte Carlo simulations as one can take advantage of different sets of paths to compute several estimates. For trees or finite differences, the computing time may be severely affected as one needs to re-run the pricing algorithm with different time or space steps.

Regressing _<sub>g</sub>_<sub>b</sub> over _<sub>g</sub>_<sub>b</sub>_c_ yields two pieces of information: (i) the slope coefficient is an estimate of _<sub>α</sub><sup>∗</sup>_, and (ii) the goodness-of-fit (_<sub>R</sub>_<sup>2</sup> coefficient) indicates the level of correlation between the numerical and the control problems and therefore validates whether or not the control variate was wisely chosen in the first place.

Another variance reduction technique is the _antithetic variate_. Suppose a first run of _<sub>N</sub>_ Monte Carlo simulations yields the estimate _<sub>g</sub>_<sub>b</sub>1\. Without simulating any other path, one can (with little extra computing time) construct _<sub>N</sub>_ additional paths by systematically replacing the values of innovations <sup>n</sup>_<sub>ε</sub>_<sup>(</sup>_<sub>k</sub><sup>j</sup>_<sub>∆</sub><sup>)</sup>_<sub>t</sub>_<sup>o</sup>_k<sup>j</sup>_<sup>\=1</sup>\=1_<sup>,...,N</sup>,...,n_

with <sup>n</sup>_−<sub>ε</sub>_<sup>(</sup>_<sub>kδt</sub><sup>j</sup>_<sup>) o</sup>_<sup>j</sup>k_<sup>\=1</sup>\=1_<sup>,...,N</sup>,...,n_ . Since the normal distribution is symmetric, the _<sub>N</sub>_ new paths are equally likely than the _<sub>N</sub>_ original ones. Let _<sub>g</sub>_<sub>b</sub>2 denote the estimator obtained from these _<sub>N</sub>_ new paths.

The antithetic variate technique consists in using

_g_b = _g_b1 +2 _g_b2 _,_

as the final estimator.

Its variance should be smaller than the variance of the original estimator. Indeed,

Var (_g_<sub>b</sub>) =  Var (_g_<sub>b</sub>1 + _g_<sub>b</sub>2) =  \[Var (_g_<sub>b</sub>1) + Var (_g_<sub>b</sub>2) + 2Cov (_g_<sub>b</sub>1_,g_<sub>b</sub>2)\]_._

Since _<sub>g</sub>_<sub>b</sub>1 and _<sub>g</sub>_<sub>b</sub>2 have the same distribution, they should have the same variance. Hence

Var (_g_<sub>b</sub>) =  \[Var (_g_<sub>b</sub>1) + Cov (_g_<sub>b</sub>1_,g_<sub>b</sub>2)\]_,_

which means the antithetic variate is a variance-reducing technique (compared to the variance of the original estimate) provided that

Cov (_g_<sub>b</sub>1_,g_<sub>b</sub>2) _<sup>≤</sup>_ Var (_g_<sub>b</sub>1)_._

This condition is satisfied for most derivative pricing problems. If the derivative payoff is a monotonic function of the UA price (like a vanilla option), then it is highly likely that Cov (_<sub>g</sub>_<sub>b</sub>1_<sub>,g</sub>_<sub>b</sub>2) _<sub>≤</sub>_ 0 (by switching the signs of innovations, a majority of ITM paths turn to OTM paths and vice versa).

**6.3 Choosing the appropriate numerical method**

Every pricing problem has their own specificity and it is hard to determine in general whether one numerical method is better suited than another. There are, however, at least three aspects of the problem that should be considered to evaluate the strengths and weaknesses of each approach.

1.  The derivative _path dependence_. The contractual payoff determines whether the value of the derivative is strongly or weakly path dependent. For instance, Asian or lookback options are strongly path dependent since their value is affected by the entire path of the UA price. By contrast, barrier options are more weakly path dependent as their value essentially depends on the current position of the UA price with respect to the activating / deactivating threshold. All else equal, Monte Carlo simulations are more appropriate to evaluate strongly path dependent derivatives, precisely because they easily map the payoff with the UA price path. By contrast, the recombining feature of trees and grids prevent such an easy mapping.
2.  The _optimal stopping_ problem. Some derivatives give the right to their holders to make a decision relative to the payoff they are receiving. When making that decision in their best interest, the derivative holders typically solve for the optimum of a free boundary problem. The obvious example is the early exercise right associated with American or Bermudian options. But one can also think of the strike resetting right associated with shout options. Numerical methods relying on backward induction (like trees and some finite differences schemes) are well designed to properly capture the trade-off between the continuation and exercise values, which characterizes the resolution of the optimal stopping problem. Nevertheless, Monte Carlo simulations can be adapted to tackle the evaluation of American options.
3.  The _dimension_ of the pricing problem. Trees and finite differences suffer from the so-called curse of dimensionality. The dynamics of two correlated state variables can be captured in a pentanomial lattice (Boyle, 1988). But when the number of underlying variables is strictly higher than two, trees become almost impossible to implement and finite differences algorithms become cumbersome. By contrast, Monte Carlo simulations easily accommodate for pricing problems in high dimension. Of course, the computing time increases with the number of state variables but the complexity of the approach does not, as the correlation structure can be handled through Cholesky decomposition.

**6.4 Problem set**

#### Exercise 6.1

Consider the American put written on an UA with current price _<sub>S</sub>_ \= 40. The put expires in a hundred trading days and its strike price is _<sub>K</sub>_ \= 42. The risk-free rate is _<sub>r</sub>_ \= 5%. The UA return volatility is _σ_ \= 25%.

1.  Under the BMS framework, evaluate the American put using the EFDM with _<sub>δS</sub>_ \= 2 and _<sub>δt</sub>_ \= 4_<sub>/</sub>_252 (i.e. four trading days). For the boundary condition at _<sub>S</sub>_ \= 0, assume the put is linear in _<sub>S</sub>_ at _S_ \= _δS_.
2.  Evaluate the American put using the same method but with _<sub>δS</sub>_ \= 1 and _<sub>δt</sub>_ \= 2_<sub>/</sub>_252\. (c) Apply Richardson extrapolation to obtain a more accurate estimate.

#### Exercise 6.2

Suppose the UA price (currently worth 100) is driven by a GBM with a 2% dividend yield and a 30% return volatility. The risk-free rate is 4%. The goal is to evaluate the 3-month American put with strike price 101 using the EFDM. Time step is set to 1 month. The space grid is made of 5 points, from 80 to 120, with a space step of 10. Boundary conditions are: (i) when the UA price is 120, the put is worthless, (ii) when the UA price is 80, the put value is the exercise value.

1.  Fill in the entire EFDM pricing grid and evaluate the American put.
2.  Compute the delta and the gamma of the American put.
3.  Suppose one wishes to evaluate the same put with the same grid but using the fully IFDM. Write down (without solving) the system of equations that determine the values of the put at the last time step but one.

#### Exercise 6.3

Suppose the UA price dynamics under the EMM is given by

d_S_(_t_) = _aS_(_t_)d_t_ \+ _σ_<sup>q</sup>_S_(_t_)d_W<sub>t</sub>,_

where _<sub>a</sub>_ and _<sub>σ</sub>_ are two positive constants and _<sub>W</sub>_(_<sub>t</sub>_) is a standard Brownian motion.

1.  Write down the no-arbitrage PDE verified by the value _<sub>g</sub>_ (_<sub>S,t</sub>_) of a derivative (let _<sub>r</sub>_ denote the constant risk-free rate).
2.  Assume _<sub>a</sub>_ \= _<sub>r</sub>_ \= 0 and _<sub>σ</sub>_ \= 0_<sub>.</sub>_2\. Consider the time and space discretization _<sub>δS</sub>_ \= 1 and _<sub>δt</sub>_ \= 1_<sub>/</sub>_100\. Write down the recursive pricing algorithm induced by the EFDM that relates _<sub>gj</sub><sup>n</sup>_ with three future values (following usual notations, subscript _<sub>j</sub>_ denotes the space position and superscript _<sub>n</sub>_ denotes the time position).
3.  Determine a constraint on the number of space steps to ensure EFDM stability, i.e. to avoid pricing anomalies.

#### Exercise 6.4

The instantaneous risk-free rate process is driven by the following square root process

d_r_(_t_) = 0_._08(0_._06 _− <sub>r</sub>_(_t_)) d_t_ \+ 0_._03<sup>q</sup>_<sub>r</sub>_(_t_)d_Z_(_t_)_,_

where _<sub>Z</sub>_ is a standard Brownian motion.

1.  Write down the simulated value _<sub>rt</sub>_<sub>+1</sub> as a function of _<sub>rt</sub>_ in a Monte Carlo simulation using the Euler discretization scheme.

The simulation of 10 paths with a weekly time step yielded the following results

_t_0 _t_1 _t_2 _t_3 _t_4 _t_5 _t_6 _t_7 _t_8

0_<sub>.</sub>_05 0_<sub>.</sub>_0498 0_<sub>.</sub>_0521 0_<sub>.</sub>_0511 0_<sub>.</sub>_0501 0_<sub>.</sub>_0513 0_<sub>.</sub>_0518 0_<sub>.</sub>_0514 0_<sub>.</sub>_0524

0_<sub>.</sub>_05 0_<sub>.</sub>_0494 0_<sub>.</sub>_0482 0_<sub>.</sub>_0483 0_<sub>.</sub>_0477 0_<sub>.</sub>_0494 0_<sub>.</sub>_0486 0_<sub>.</sub>_0479 0_<sub>.</sub>_0481

0_<sub>.</sub>_05 0_<sub>.</sub>_0504 0_<sub>.</sub>_0506 0_<sub>.</sub>_0492 0_<sub>.</sub>_0513 0_<sub>.</sub>_0515 0_<sub>.</sub>_0523 0_<sub>.</sub>_0514 0_<sub>.</sub>_0512

0_<sub>.</sub>_05 0_<sub>.</sub>_0491 0_<sub>.</sub>_0475 0_<sub>.</sub>_0471 0_<sub>.</sub>_0472 0_<sub>.</sub>_0467 0_<sub>.</sub>_0471 0_<sub>.</sub>_0488 0_<sub>.</sub>_0501

0_<sub>.</sub>_05 0_<sub>.</sub>_0495 0_<sub>.</sub>_0487 0_<sub>.</sub>_0471 0_<sub>.</sub>_0449 0_<sub>.</sub>_0438 0_<sub>.</sub>_0429 0_<sub>.</sub>_0414 0_<sub>.</sub>_0409

0_<sub>.</sub>_05 0_<sub>.</sub>_0506 0_<sub>.</sub>_0511 0_<sub>.</sub>_0523 0_<sub>.</sub>_0523 0_<sub>.</sub>_0523 0_<sub>.</sub>_0525 0_<sub>.</sub>_0524 0_<sub>.</sub>_0534

0_<sub>.</sub>_05 0_<sub>.</sub>_0485 0_<sub>.</sub>_0471 0_<sub>.</sub>_0483 0_<sub>.</sub>_0484 0_<sub>.</sub>_0508 0_<sub>.</sub>_0498 0_<sub>.</sub>_0482 0_<sub>.</sub>_0473

0_<sub>.</sub>_05 0_<sub>.</sub>_0491 0_<sub>.</sub>_0495 0_<sub>.</sub>_0502 0_<sub>.</sub>_0495 0_<sub>.</sub>_0489 0_<sub>.</sub>_0493 0_<sub>.</sub>_0472 0_<sub>.</sub>_0467

0_<sub>.</sub>_05 0_<sub>.</sub>_0510 0_<sub>.</sub>_0520 0_<sub>.</sub>_0518 0_<sub>.</sub>_0540 0_<sub>.</sub>_0550 0_<sub>.</sub>_0552 0_<sub>.</sub>_0561 0_<sub>.</sub>_0573

0_<sub>.</sub>_05 0_<sub>.</sub>_0496 0_<sub>.</sub>_0479 0_<sub>.</sub>_0476 0_<sub>.</sub>_0470 0_<sub>.</sub>_0474 0_<sub>.</sub>_0466 0_<sub>.</sub>_0474 0_<sub>.</sub>_0464

1.  Compute the premium of the down-and-in put written on the risk-free rate, expiring in 8 weeks, with a 5% strike and a 4.7% barrier (assume the barrier observation frequency is weekly).

#### Exercise 6.5

The UA current price _<sub>S</sub>_ lies within \[_<sub>a,b</sub>_\]. Let _<sub>τ</sub>_ denote the first time _<sub>S</sub>_(_<sub>t</sub>_) gets out of \[_<sub>a,b</sub>_\]. Formally,

_τ_ \= _{_inf _t ≥_ 0 : _S_(_t_) _≥ b_ or _S_(_t_) _≤ a}._

Let _<sub>θ</sub>_ \= inf (_<sub>τ,T</sub>_). For a given observation period, the boost option with expiration date _<sub>T</sub>_ offers $_<sub>M</sub>_ at time _<sub>θ</sub>_ where _<sub>M</sub>_ denotes the number of periods spent within \[_<sub>a,b</sub>_\]. In the AoA, its value is therefore given by _g_ \= E<sup>Q</sup> \[exp(_−rθ_) _× M_\]_._

(a) Assuming the UA price is driven by a GBM with no dividend and 25% volatility, write down the simulated value _<sub>S</sub>_(_<sub>t</sub>_+_<sub>δt</sub>_) as a function of _<sub>S</sub>_(_<sub>t</sub>_) in a Monte Carlo simulation using the Euler discretization scheme. The risk-free rate is 5%.

The Monte Carlo simulation of 10 paths over 8 weeks for the UA price under the EMM yielded the following results

100 101_<sub>.</sub>_32 106_<sub>.</sub>_81 102_<sub>.</sub>_40 104_<sub>.</sub>_76 106_<sub>.</sub>_91 108_<sub>.</sub>_54 106_<sub>.</sub>_32 108_<sub>.</sub>_82

100 105_<sub>.</sub>_73 107_<sub>.</sub>_52 106_<sub>.</sub>_16 107_<sub>.</sub>_92 112_<sub>.</sub>_73 119_<sub>.</sub>_06 119_<sub>.</sub>_65 113_<sub>.</sub>_83 100 97_<sub>.</sub>_88 99_<sub>.</sub>_93 99_<sub>.</sub>_87 99_<sub>.</sub>_42 99_<sub>.</sub>_19 104_<sub>.</sub>_95 102_<sub>.</sub>_96 107_<sub>.</sub>_37

100 96_<sub>.</sub>_85 99_<sub>.</sub>_57 97_<sub>.</sub>_53 95_<sub>.</sub>_79 94_<sub>.</sub>_51 91_<sub>.</sub>_86 91_<sub>.</sub>_30 91_<sub>.</sub>_28 100 98_<sub>.</sub>_30 102_<sub>.</sub>_16 101_<sub>.</sub>_94 104_<sub>.</sub>_39 95_<sub>.</sub>_03 91_<sub>.</sub>_36 93_<sub>.</sub>_79 92_<sub>.</sub>_77 100 97_<sub>.</sub>_04 91_<sub>.</sub>_42 89_<sub>.</sub>_95 84_<sub>.</sub>_26 77_<sub>.</sub>_12 74_<sub>.</sub>_84 75_<sub>.</sub>_25 80_<sub>.</sub>_09

100 94_<sub>.</sub>_89 91_<sub>.</sub>_37 91_<sub>.</sub>_49 95_<sub>.</sub>_60 90_<sub>.</sub>_73 90_<sub>.</sub>_75 89_<sub>.</sub>_55 87_<sub>.</sub>_85 100 104_<sub>.</sub>_42 101_<sub>.</sub>_40 97_<sub>.</sub>_52 93_<sub>.</sub>_49 90_<sub>.</sub>_84 89_<sub>.</sub>_19 88_<sub>.</sub>_97 86_<sub>.</sub>_08 100 97_<sub>.</sub>_58 101_<sub>.</sub>_14 99_<sub>.</sub>_41 103_<sub>.</sub>_71 107_<sub>.</sub>_41 105_<sub>.</sub>_30 101_<sub>.</sub>_06 99_<sub>.</sub>_55 100 98_<sub>.</sub>_37 99_<sub>.</sub>_35 95_<sub>.</sub>_34 93_<sub>.</sub>_36 91_<sub>.</sub>_47 96_<sub>.</sub>_13 91_<sub>.</sub>_63 91_<sub>.</sub>_86 (b) Compute the premium of the boost option with boundaries \[_<sub>a,b</sub>_\] = \[96_<sub>,</sub>_104\] and weekly observation frequency (the payoff is the number of complete weeks, i.e., _<sub>M</sub>_ \= 52 _<sub>×</sub>_ (_<sub>θ −</sub>_ 1)).

#### Exercise 6.6

The Monte Carlo simulation generated the five following paths

~~Date 0 1 month 2 months 3 months 4 months~~

Path #1 100 101.27 99.05 99.97 102.14 Path #2 100 98.82 100.57 103.11 102.90

Path #3 100 100.05 101.44 98.04 96.56

Path #4 100 102.22 103.29 101.55 104.05

Path #5 100 98.53 99.36 100.98 97.64

The goal is to evaluate the ATM, 4-month American call written on the simulated UA using the Longstaff and Schwartz (2001) regression approach. The risk-free rate is 3%. Suppose the regressions estimating the continuation values are the following

0_<sub>.</sub>_002_<sub>S</sub>_<sup>2</sup> _−_ 0_<sub>.</sub>_12_<sub>S</sub> −_ 7 for _<sub>t</sub>_ \= 3 months,

0_<sub>.</sub>_001_<sub>S</sub>_<sup>2</sup> _−_ 0_<sub>.</sub>_08_<sub>S</sub> −_ 1 for _<sub>t</sub>_ \= 2 months, 0_<sub>.</sub>_001_<sub>S</sub>_<sup>2</sup> _−_ 0_<sub>.</sub>_12_<sub>S</sub>_ \+ 3 for _<sub>t</sub>_ \= 1 month.

1.  For each path, determine the optimal exercise date.
2.  Compute the initial value of the call.

#### Exercise 6.7

Below are two simulated paths of the GBM with drift 0.04 and diffusion coefficient 0.2.

##### ~~Date 0 Month 1 Month 2 Month 3 Month 4~~

Path #1 100 103.12 98.56 99.07 102.44

Path #2 100 97.81 101.87 100.13 99.25

1.  Assuming these paths correspond to those of the price of an UA without dividends, compute the value of the lookback put with 4-month maturity and strike 101, written on the minimum UA price, observed every month since today till maturity.
2.  Apply the antithetic variate method to construct two additional paths.
3.  Give a better estimate for the lookback put premium.

**6.5 Solutions**

#### Solution 6.1

1.  Using _<sub>δS</sub>_ \= 2 and _<sub>δt</sub>_ \= 4_<sub>/</sub>_252, one gets

_P_<sub>1</sub> 0_,_ <sup>100</sup>252_,_42 \= 3_._28544_._

1.  Using _<sub>δS</sub>_ \= 1 and _<sub>δt</sub>_ \= 1_<sub>/</sub>_252, one gets

_P_<sub>2</sub> 0_,_ 100252_,_42 = 3_._29816_._

1.  The ratio _<sub>δt/</sub>_(_<sub>δS</sub>_)<sup>2</sup> is the same in the first two questions. Hence Richardson extrapolation yields

4_P_42_−−_1_P_1 = 3_._30239_._

#### Solution 6.2

(a) According to the boundary conditions, the pricing grid looks like this

_t_ \= 0 _<sub>t</sub>_ \=  _<sub>t</sub>_ \=  _<sub>t</sub>_ \= 

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | _S_ \= 120 |
|     |     |     | 0   | _S_ \= 110 |
|     |     |     | 1   | _S_ \= 100 |
|     |     |     | 11  | _S_ \= 90 |
| 21  | 21  | 21  | 21  | _S_ \= 80 |

The EFDM algorithm is

_gjn − gjn_+1 + _gjn_+12_−<sub>δS</sub>gjn−_1 (_<sub>r − y</sub>_)_<sub>iδS</sub>_ \+ <sup>1</sup>2 _gjn_+1 (_<sub>δS</sub>_)<sub>2</sub> _gjn−_1 _<sub>σ</sub>_2 (_<sub>iδS</sub>_)2 = _<sub>rgj</sub>n<sub>.</sub>_

_<sub>δt</sub>_

The numerical application yields

_gjn − gjn_+1 + _gjn_+1 _− gjn−_1_i_ \+ _gjn_+1 _−_ 2_gjn_ \+ _gjn−_1 024_._09_i_2 = _gjn,_

or, alternatively,

_gj j−_1 24_. i_2 _−_ 24 _i_ + _gjn_ 1112_._96 _−_ 024_._18_i_2 _n_+1 = _gn_ 0 09 0_._02

+_gjn_+1 _i_ \+ _i_2_._

Thus,

_g_<sub>9</sub>1 = 21024_._0992 _−_ 024_._029 + 11 _−_ 024_._1892 + 1024_._029 + 2 = 10_<sub>.</sub>_813 _g_101 = 11024_._09102 _−_ 024_._0210 + 1 _−_ 102 + 0024_._0210 + 10<sup>2</sup>

9

|     |     |
| --- | --- |
| \=  | 4_<sub>.</sub>_28 |

_g_111 = 1024_._09112 _−_ 024_._0211 + 0 _−_ 112 + 0024_._0211 + 11<sup>2</sup> = 0_<sub>.</sub>_44458

Comparing with exercise values, we correct for _<sub>g</sub>_<sub>9</sub><sup>1</sup> \= 11. Then, _g_<sub>9</sub>2 = 21024_._0992 _−_ 024_._029 + 11 _−_ 024_._1892 + 4_._28024_._029 + 2

9

|     |     |
| --- | --- |
| \=  | 11_<sub>.</sub>_834 |

_g_102 = 11024_._09102 _−_ 024_._0210 + 4_._28 _−_ 102 + 0_._44458024_._0210 + 10<sup>2</sup>

|     |     |
| --- | --- |
| \=  | 5_<sub>.</sub>_2595 |

_g_112 = 4_._28024_._09112 _−_ 024_._0211 + 0_._44458 _−_ 112 + 0024_._0211 + 11<sup>2</sup> = 1_<sub>.</sub>_9425

No exercise value exceeds those continuation values. Finally, _<sup>g</sup>_93 = 21024_._0992 _−_ 024_._029 + 11_._834 _−_ 024_._1892 + 5_._2595024_._029 + 024_._0992

|     |     |
| --- | --- |
| \=  | 12_<sub>.</sub>_464 |

_g_103 = 11_._834024_._09102 _−_ 024_._0210 + 5_._2595 _−_ 102 + 1_._9425024_._0210 + 102 = 6_<sub>.</sub>_3811

_g_113 = 5_._2595024_._09112 _−_ 024_._0211 + 1_._9425 _−_ 112 + 0024_._0211 + 112 = 2_<sub>.</sub>_5115

No exercise value exceeds those continuation values. Hence the completed pricing grid is

_t_ \= 0 _<sub>t</sub>_ \=  _<sub>t</sub>_ \=  _<sub>t</sub>_ \= 

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | _S_ \= 120 |
| 2.5115 | 1.9425 | 0.44458 | 0   | _S_ \= 110 |
| 6.3811 | 5.2595 | 4.28 | 1   | _S_ \= 100 |
| 12.464 | 11.834 | 11  | 11  | _S_ \= 90 |
| 21  | 21  | 21  | 21  | _S_ \= 80 |

The American put is currently worth 6.3811.

1.  The delta can be proxied by

∆ =  (2_<sub>.</sub>_5115 _−_ 12_<sub>.</sub>_464) = _−_0_<sub>.</sub>_49763_<sub>.</sub>_

The gamma can be proxied by

Γ =  (2_<sub>.</sub>_5115 _<sub>−</sub>_ 6_<sub>.</sub>_3811 _<sub>−</sub>_ 6_<sub>.</sub>_3811 + 12_<sub>.</sub>_464) = 0_<sub>.</sub>_022133_<sub>.</sub>_

1.  The fully IFDM algorithm is

_gjn−_1 _− gjn_ \+ _gjn_+12_−<sub>δS</sub>gjn−_1 (_<sub>r − y</sub>_)_<sub>iδS</sub>_ \+ <sup>1</sup>2 _gjn_+1 (_<sub>δS</sub>_)<sub>2</sub> _gjn−_1 _<sub>σ</sub>_2 (_<sub>iδS</sub>_)2 = _<sub>rgj</sub>n<sub>.</sub>_

_<sub>δt</sub>_

The numerical application yields

_gjn−_1 _− gjn_ \+ _gjn_+1 _− gjn−_1_i_ \+ _gjn_+1 _−_ 2_gjn_ \+ _gjn−_1 024_._09_i_2 = _gjn,_

that is,

_gj j−_1 _−_024 _i_2 + 024_._02_i_ + _gjn_ +_i_2 _n−_1 = _gn ._09

+_gjn_+1 _−_024_._02_i −_ 024_._09_i_2_._

The 3-unknown, 3-equation system is

- 1.  \= _g_101 _−_024_<sub>.</sub>_09112 + 024_<sub>.</sub>_0211 + _g_111  + 112 + _g_121 _−_024_<sub>.</sub>_0211 _−_ 11<sup>2</sup>_,_
    2.  \= _g_91 _−_024_<sub>.</sub>_09102 + 024_._0210 + _g_101 1212_._04 + 024_._18102 + _g_111 _−_024_._0210 _−_ 10<sup>2</sup>_,_

11 = _g_81 _−_024_<sub>.</sub>_0992 + 024_._029 + _g_91 1212_._04 + 024_._1892 + _g_101 _−_024_._029 _−_ 92_,_

or, alternatively,

- - 1.  \= _−_0_._44458 _× g_<sub>10</sub><sup>1</sup> _−_  _× g_<sub>11</sub><sup>1</sup> _,_
        2.  \= _−_0_._36667 _× g_<sub>9</sub><sup>1</sup> _−_  _× g_<sub>10</sub><sup>1</sup> _−_ 0_._38333 _× g_<sub>11</sub><sup>1</sup> _,_

11 = _−_6_._2213 _−_  _× g_<sub>9</sub><sup>1</sup> _−_ 0_._31125 _× g_<sub>10</sub><sup>1</sup> _._

#### Solution 6.3

1.  The no-arbitrage PDE is

_rg_ _S._

1.  According to the EFDM, the discretized PDE is

0 = 100_gjn − gjn_+1 + 0_._02_gjn_+1 _−_ 2_gjn_ \+ _gjn−_1_i,_

that is,

_g<sub>j</sub><sup>n</sup>_<sup>+1</sup> \= _g<sub>j</sub><sup>n</sup>_<sub>+1</sub>0_._0002_i_ \+ _g<sub>j</sub><sup>n</sup>_ (1 _−_ 0_._0004_i_) + _g<sub>j</sub><sup>n</sup><sub>−</sub>_<sub>1</sub>0_._0002_i._

1.  For the algorithm to be stable, we require that

1 _−_ 0_._0004_i >_ 0_,_ 0_._0002_i <_ 1_,_

which yields

_i <_ 2500_._

#### Solution 6.4

1.  The simulated process is

_r<sub>t</sub>_<sub>+1</sub> \= _r<sub>t</sub>_ \+ 0_._08(0_._06 _− r<sub>t</sub>_)_δt_

+0_._03p_rtδt_q_−_2lnRandom()cos(2_π_Random())_,_

where <sub>Random</sub>() is a function returning a draw from the uniform law on \[0_<sub>,</sub>_1\].

1.  The put is activated for paths #4, 5, 8 and 10, only. Regarding path #4, the option expires worthless. As far as the three other paths are concerned, the terminal payoffs (0.91%, 0.33%, and 0.36%, respectively) are discounted with the average rate from date _<sub>t</sub>_<sub>0</sub> till date _<sub>t</sub>_<sub>7</sub>, which yields

_g__._

#### Solution 6.5

1.  The simulated process is

)

 _S<sub>t</sub>δtε ,_

with _ε_ \= q_−_2lnRandom()cos(2_π_Random())_._

1.  The table below summarizes the payoffs associated with each path

|     |     |
| --- | --- |
| Path _<sub>N</sub>_ Path | _N_ |
| 1 1 _×_ 52 6 | 1 _×_ 52 |
| 2 0 _×_ 52 7 | 0 _×_ 52 |
| 3 5 _×_ 52 8 | 0 _×_ 52 |
| 4 3 _×_ 52 9 | 4 _×_ 52 |
| 5 3 _×_ 52 10 | 2 _×_ 52 |

The premium of the boost option is therefore estimated at

_._

#### Solution 6.6

(a) At month 3, continuation values are

0_<sub>.</sub>_002 _×_ 99_<sub>.</sub>_97<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 99_<sub>.</sub>_97 _−_ 7 = 0_<sub>.</sub>_9916_<sub>,</sub>_

0_<sub>.</sub>_002 _×_ 103_<sub>.</sub>_11<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 103_<sub>.</sub>_11 _−_ 7 = 1_<sub>.</sub>_8901_<sub>,</sub>_

0_<sub>.</sub>_002 _×_ 98_<sub>.</sub>_04<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 98_<sub>.</sub>_04 _−_ 7 = 0_<sub>.</sub>_45888_<sub>,</sub>_

0_<sub>.</sub>_002 _×_ 101_<sub>.</sub>_55<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 101_<sub>.</sub>_55 _−_ 7 = 1_<sub>.</sub>_4388_<sub>,</sub>_

0_<sub>.</sub>_002 _×_ 100_<sub>.</sub>_98<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 100_<sub>.</sub>_98 _−_ 7 = 1_<sub>.</sub>_2763_<sub>.</sub>_

Early exercise therefore occurs for paths # 2 and 4. At month 2, continuation values are

0_<sub>.</sub>_001 _×_ 99_<sub>.</sub>_05<sup>2</sup> _−_ 0_<sub>.</sub>_08 _×_ 99_<sub>.</sub>_05 _−_ 1 = 0_<sub>.</sub>_8869_<sub>,</sub>_

0_<sub>.</sub>_001 _×_ 100_<sub>.</sub>_57<sup>2</sup> _−_ 0_<sub>.</sub>_08 _×_ 100_<sub>.</sub>_57 _−_ 1 = 1_<sub>.</sub>_0687_<sub>,</sub>_

0_<sub>.</sub>_001 _×_ 101_<sub>.</sub>_44<sup>2</sup> _−_ 0_<sub>.</sub>_08 _×_ 101_<sub>.</sub>_44 _−_ 1 = 1_<sub>.</sub>_1749_<sub>,</sub>_

0_<sub>.</sub>_001 _×_ 103_<sub>.</sub>_29<sup>2</sup> _−_ 0_<sub>.</sub>_08 _×_ 103_<sub>.</sub>_29 _−_ 1 = 1_<sub>.</sub>_4056_<sub>,</sub>_ 0_<sub>.</sub>_001 _×_ 99_<sub>.</sub>_36<sup>2</sup> _−_ 0_<sub>.</sub>_08 _×_ 99_<sub>.</sub>_36 _−_ 1 = 0_<sub>.</sub>_92361_<sub>.</sub>_

Early exercise therefore occurs for paths # 3 and 4. At month 1, continuation values are

0_<sub>.</sub>_001 _×_ 101_<sub>.</sub>_27<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 101_<sub>.</sub>_27 + 3 = 1_<sub>.</sub>_1032_<sub>,</sub>_

0_<sub>.</sub>_001 _×_ 98_<sub>.</sub>_82<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 98_<sub>.</sub>_82 + 3 = 0_<sub>.</sub>_90699_<sub>,</sub>_

0_<sub>.</sub>_001 _×_ 100_<sub>.</sub>_05<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 100_<sub>.</sub>_05 + 3 = 1_<sub>.</sub>_004_<sub>,</sub>_

0_<sub>.</sub>_001 _×_ 102_<sub>.</sub>_22<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 102_<sub>.</sub>_22 + 3 = 1_<sub>.</sub>_1825_<sub>,</sub>_

0_<sub>.</sub>_001 _×_ 98_<sub>.</sub>_53<sup>2</sup> _−_ 0_<sub>.</sub>_12 _×_ 98_<sub>.</sub>_53 + 3 = 0_<sub>.</sub>_88456_<sub>.</sub>_

Early exercise therefore occurs for paths # 1 and 4.

Thus, optimal exercise dates are

|     |     |
| --- | --- |
| Month 1 | for path #1, |
| Month 3 | for path #2, |
| Month 2 | for path #3, |
| Month 1 | for path #4, |
| Month 4 | for path #5. |

(b) The American call is worth today

1_._27_e−_0_._03 + 3_._11_e−_0_._03 + 1_._44_e−_0_._03 + 2_._22_e−_0_._03 + 0_/_5 = 1_._6002_._

#### Solution 6.7

1.  The observed minimum along path #1 is 98.56. Hence

_g_<sup>(1)</sup> \= (101 _−_ 98_._56)_e<sup>−</sup>_<sup>0</sup>_<sup>.</sup>_<sup>04</sup> = 2_._4077_._

The observed minimum along path #2 is 97.81. Hence

_g_<sup>(2)</sup> \= (101 _−_ 97_._81)_e<sup>−</sup>_<sup>0</sup>_<sup>.</sup>_<sup>04</sup> = 3_._1477_._

The lookback put is therefore estimated at

_ga_ \= <sup>2</sup>_<sup>.</sup>_ \= 2_<sub>.</sub>_7777_<sub>.</sub>_

1.  Simulations have been generated by

_S_(_t_ \+ _δt_) = _S_(_t_)exp" 0_._04 _−_ 0_._222 ! 121 + _√_0_._~~12~~2 _ε_#_,_

where _<sub>ε</sub>_ stands for the standard normal innovation. Thus, at each time step,

_√_ " 2 ! #

_ε_ \= 0_._~~12~~2 ln _S_(_St_ +(_t_)_δt_) _−_ 0_._04 _−_ 0_._22 121 _,_

that is,

)

\= 10

_√_

3

ln

_S_

(

_t_

+

_δt_

_S_

(

_t_

)

_−_

1

20

_√_

3

_ε._

The realized draws of _<sub>ε</sub>_ corresponding to the two paths are therefore

~~Date Month 1 Month 2 Month 3 Month 4~~

Path #1 0.50327 -0.81224 0.06053 0.55051

Path #2 -0.41240 0.67557 -0.32727 -0.18176

Antithetic draws are

##### ~~Date Month 1 Month 2 Month 3 Month 4~~

Path #3 -0.50327 0.81224 -0.06053 -0.55051 Path #4 0.41240 -0.67557 0.32727 0.18176

and the corresponding UA prices are

_,_

which yields

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| ~~Date~~ | ~~0~~ | ~~Month 1~~ | ~~Month 2~~ | ~~Month 3~~ | ~~Month 4~~ |
| Path #3 | 100 | 97.29821 | 102.13975 | 101.95321 | 98.92846 |
| Path #4 | 100 | 102.58039 | 98.82093 | 100.87388 | 102.10805 |

(c) The observed minimum along path #3 is 97.30. Hence

_g_<sup>(3)</sup> \= (101 _−_ 97_._30)_e<sup>−</sup>_<sup>0</sup>_<sup>.</sup>_<sup>04</sup> = 3_._651_._

The observed minimum along path #4 is 98.82. Hence

_g_<sup>(4)</sup> \= (101 _−_ 98_._82)_e<sup>−</sup>_<sup>0</sup>_<sup>.</sup>_<sup>04</sup> = 2_._1511_._

The value of the lookback put based on paths #3 and 4 is

_gb_ \= 3_._ \= 2_._9011_._

A better estimate of the lookback put premium is

_g_ \= _ga_ +2 _gb ,_

that is,

_g_ \= 2_._ \= 2_._8394_._

**Chapter 7**

**Modeling volatility**

In this chapter, we discuss one of the main limitations of the BMS model: the constant volatility assumption. One way of indirectly testing this assumption consists in inverting the explicit formula of the BMS model to infer the volatility parameter which is consistent with the observed option price. The resulting value is coined the _implied volatility_. According to the BMS model, the volatility parameter should be the same for all option contracts written on the same underlying. In the first part of this chapter, we discuss a robust stylized fact: this feature is violated in practice. Depending on the type of underlying and the market conditions, implied volatilities vary across the option strikes and maturities. As a result, the set of all implied volatilities inferred from all option contracts on the same underlying defines the implied volatility surface. A curve from this surface at a given maturity is referred to as the implied volatility _smile_ (or _smirk_). Fixing the strike (e.g., ATM) and varying the maturity yields a _term structure_ of implied volatilities.

There are several methods to reconcile an option valuation model with the implied volatility surface in practice. Among these methods, one consists in accounting for the time varying nature of the historical volatility, which has been highlighted by several studies including Bollerslev et al. (1992). Even under conditional normality, heteroscedasticity generates non-normal distributions at horizons relevant to option pricing; this non-normality can (partly) explain the shape of the implied volatility surface.

In this spirit, various volatility models have been used to value options including GARCH, stochastic volatility and CEV models. GARCH models assume an autoregressive dynamics for the volatility. The second part of this chapter is devoted to an in-depth study of this family of models with a particular emphasis on the non-affine GARCH(1,1) model. GARCH models are good approximations, but approximations nonetheless, of continuous time stochastic volatility models (see Nelson (1990)). We study such stochastic volatility models in the third part of this chapter. We emphasize that market incompleteness arises in such models since the volatility of the underlying is assumed to have its own source of randomness. To avoid working in an incomplete market framework, the family of constant elasticity of variance models (CEV models) suggests to link the volatility directly to the level of the underlying. We study these models in the fourth part of this chapter.

In this fifth part of this chapter, we study a last approach in which the implied volatility is explicitly modeled. One simple way of implementing this idea is to consider the implied volatility as a deterministic process. This approach is however found to perform poorly in terms of pricing errors. Some alternative

189

approaches model the implied volatility by using a stochastic process.

It is worth stressing that other arguments, which are beyond the scope of this chapter, have been put forward to explain the existence of an implied volatility surface. This includes constraints linked to the liquidity of market options, the frequency of rebalancing of the replication portfolio (see Bossaerts and Hillion (1997)) or the effects of microstructure (Platen and Schweizer (1998)).

**7.1 Implied volatility surface**

The BMS option pricing formula provides a bijection between the option price and the volatility of the underlying returns which is assumed to be constant. More precisely, if we observe the market price _<sub>Omkt</sub>_ of European option, we have that

_O_(_t,T,K |S,r,y,σ_) = _π<sub>bms</sub>_(_σ_) = _O<sub>mkt</sub>_

where _<sub>πbms</sub>_ stands for the BMS pricing formula with all parameters other than _<sub>σ</sub>_ taken as given. Since _π<sub>bms</sub>_ is stricly increasing in _<sub>σ</sub>_, we have that

_σ_ \= _πbms<sup>−</sup>_<sup>1</sup> (_O<sub>mkt</sub>_)_._

According to the BMS model, inverting the BMS price function should yield the same volatility output for all options that are written on the same underlying. However, this is not the case in practice. Rubinstein (1985) is the first important study documenting this counterfactual evidence against the BMS framework.

Before the October 1987 financial crash, the graph of implied volatilities as a function of strike prices was (for most types of UA) U-shaped and centered around the ATM strike price. Such a phenomenon is referred to as a (volatility) _smile_: the BMS model tends to underestimate OTM options. A possible explanation for this feature could be that the empirical distribution of the underlying log-returns does not follow a normal distribution. Rather, the tails are fatter (leptokurtic distribution), which implies that OTM options are more expensive than what the BMS model would suggest (cf. Figures 7.1 and 7.2).

Figure

39

Implied volatility

0

K / S

1

Figure 7.1: Implied volatility smile.

Figure

40

Normal

distribution

Leptokurtic

distribution

Figure 7.2: Leptokurtic risk-neutral distribution.

For some UAs, the smile gets asymmetric (cf. Figure 7.3). For instance, since the October 1987 market crash, the smile on the S&P 500 typically exhibits a decreasing shape as illustrated below. This type of smile is sometimes referred to as a _smirk_, a _sneer_, or a _skew_: OTM puts (_<sub>K/S <</sub>_ 1) are associated with higher implied volatilities than OTM calls (_<sub>K/S ></sub>_ 1).

Figure

41

Implied volatility

0

K / S

1

Figure 7.3: Asymmetric implied volatility smile (aka _smirk_, _sneer_, or _skew_).

As far as the maturity effect is concerned, the smile or the smirk tend to flatten for long-maturity options. Figure 7.4 below represents a typical shape of the implied volatility surface.

Figure

42

Implied volatility

Moneyness

Maturity

Figure 7.4: Implied volatility surface.

In practice, only a limited number of options are traded. Consequently, the implied volatility surface is only partially observed at discrete points, and the smile shows up irregularly. Figure 7.5 reports the implied volatility smiles for call options written on the IBM stock traded on the Chicago Board Of Exchange on April 20, 2005. The underlying closed at 72.01 on this date.

simp

Figure 7.5: April 20, 2005, implied volatility smiles on IBM stock, at different maturities.

Implied volatilities (_<sub>σimp</sub>_) as a function of the strike price (_<sub>K</sub>_) are reported for call options expiring by the end of June 2005 (bold line), July 2005 (thick line), October 2005 (thick dotted line), January 2006 (medium dotted line), and January 2007 (large dotted line). Despite some irregularities, we see how the different smiles flatten as the maturity of the option increases.

On a given day, the set of traded options (and therefore observable implied volatilities) can be grouped into a moneyness / maturity matrix. Implied volatilities beyond available market data can be obtained from interpolation. The simplest method is bilinear interpolation that we now illustrate. Consider the following implied volatility matrix (in percentage points)

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| _S/K_ | 0_<sub>.</sub>_90 | 0_<sub>.</sub>_95 | 1_<sub>.</sub>_00 | 1_<sub>.</sub>_05 | 1_<sub>.</sub>_10 |
| _T_ \= 121<br><br>_T_ \= 123<br><br>_T_ \= 126<br><br>_T_ \= 1 | 23_<sub>.</sub>_4<br><br>23_<sub>.</sub>_2<br><br>23_<sub>.</sub>_0<br><br>23_<sub>.</sub>_1 | 22_<sub>.</sub>_7<br><br>22_<sub>.</sub>_6<br><br>22_<sub>.</sub>_8<br><br>22_<sub>.</sub>_7 | 22_<sub>.</sub>_2<br><br>22_<sub>.</sub>_4<br><br>22_<sub>.</sub>_3<br><br>22_<sub>.</sub>_5 | 22_<sub>.</sub>_6<br><br>22_<sub>.</sub>_6<br><br>22_<sub>.</sub>_5<br><br>22_<sub>.</sub>_6 | 22_<sub>.</sub>_9<br><br>22_<sub>.</sub>_8<br><br>22_<sub>.</sub>_7<br><br>22_<sub>.</sub>_6 |

Suppose the current UA price is 100 and we want to evaluate an option with a strike of 98 and 4 months to expiration. Let _<sub>x</sub>_ denote the implied volatility for that option. The four closest coordinates are

_S/K_ \= 1, _<sub>S/K</sub>_ \= 1_<sub>.</sub>_05, _<sub>T</sub>_ \= 3_<sub>/</sub>_12 and _<sub>T</sub>_ \= 6_<sub>/</sub>_12, defining a rectangle (_<sub>a</sub>_<sub>1</sub>_<sub>,a</sub>_<sub>2</sub>_<sub>,a</sub>_<sub>3</sub>_<sub>,a</sub>_<sub>4</sub>) around the implied volatility _<sub>x</sub>_, as shown of Figure 7.6.

Figure

44

_S/K =_

1.00

_S/K =_

1.05

_T =_

12

6

/

_T =_

12

/

3

_K =_

100/98

_T =_

12

/

4

_A_

1

_A_

4

_A_

3

_A_

2

**a1**

**a2**

**a3**

**a4**

**_x_**

Figure 7.6: Visualization of the bilinear interpolation approach.

The bilinear interpolation consists in weighting every corner _<sub>ai</sub>_ by the area _<sub>Ai</sub>_ of the ”opposite” rectangle

(i.e., the one with diagonal _<sub>x</sub>_ and the corner _<sub>aj</sub>_ opposite to _<sub>ai</sub>_). That is,

P4 _x_ \= P_i_\=14 _aiAi ._

_i_\=1 _Ai_

In our example, this yields

<sup>6</sup>

 _x_ _<sub>−</sub>_(1_._05 _−_ 1_._00) = 22_._4_<sub>−</sub>_1_._05 _−_ <sup>100</sup>98

12

+22_._6 _−_ 124  _−_ 1_._00

+22_._5 _−_ 123  _−_ 1_._00 +22_._3 _−_ 1_._05 _−_ 10098 _,_

that is, _x_ \= 22_<sub>.</sub>_448%_<sub>.</sub>_

Of course, nonlinear interpolation schemes can also be used for enhanced accuracy.

The implied volatility surface is informative about the _risk-neutral_ distribution of the UA, as initially noted by Breeden and Litzenberger (1978). In the AoA, the premium for a European call is given by

Z _∞_

_c_(_t,T,K_) = _e−r_(_T−t_) (_ST − K_)_ft_ (_ST_ )_dST ,_

_K_

where the _<sub>ft</sub>_ (_<sub>.</sub>_) function denotes the time-_<sub>t</sub>_ conditional density of _<sub>ST</sub>_ under the EMM Q. By differentiating this equation twice with respect to the strike price, we obtain

_∂_2_c_(_t,T,K_)Z _∞_ (_ST_ )_dST_ \= _e−r_(_T−t_)_ft_ (_K_)_. f_

_∂K_2 _∂K K t_

Hence, for every moneyness point _<sub>x</sub>_ along the _<sub>T</sub>_\-maturity smile,

_t,T,x_) _f<sub>t</sub> ._

Thus, we can obtain a point by point approximation of the function _<sub>ft</sub>_(_<sub>.</sub>_) by discretizing the second derivative of the European call premium with respect to the strike price

_<sub>f</sub>t_(_<sub>x</sub>_) _≃ <sub>e</sub>r_<sub>(</sub>_<sub>T−t</sub>_<sub>)</sub> _c_(_t,T,x_ \+ _δK_) _−_ 2_c_((_<sub>δK</sub>t,T,x_)2 ) + _c_(_S,T,x − δK_)_<sub>,</sub>_

where _<sub>δK</sub>_ is a arbitrarily small. Interestingly, the numerator is a (long call) butterfly spread.

**7.2 GARCH models**

The GARCH (short for _Generalized AutoRegressive Conditional Heteroscedasticity_) family of models was first introduced by Bollerslev (1986). Although GARCH volatility models are used in a many other contexts, we will here present them as a generalization of BMS, in discrete time, that allows for dynamic volatility. GARCH models are simple, and straightforward to estimate and to implement, which contributes to their popularity among practitioners as well as academics.

Consider the Euler discretization of the BMS model under the physical probability mesure between time 0 and _<sub>T</sub>_ :<sup><sup>[\[6\]](#footnote-6)</sup></sup>

_S_ ((_t_ \+ 1)_δ_) = _S_ (_tδ_)exp_<sub>µ,</sub>_ (7.1)

where _t_ \= 0_,...,T −_ 1, _T_ \= _T /δ_ and _{ε<sub>tδ</sub>}<sup>T</sup><sub>t</sub>_<sub>\=1</sub> are i.i.d. standard normal innovations.

For a given observation frequency, say, a day, a month, or a quarter (_<sub>δ ∈ {</sub>_1_<sub>/</sub>_252_<sub>,</sub>_1_<sub>/</sub>_12_<sub>,</sub>_1_<sub>/</sub>_4_<sub>}</sub>_), we can express the model in terms of this frequency:

_S<sub>t</sub>__<sub>,</sub>_ (7.2)

_√_

where _S<sub>t</sub> ≡ S_(_tδ_), _µ<sub>δ</sub> ≡ µδ_, and _σ<sub>δ</sub> ≡ σ δ_. Define log-returns as

_r<sub>t</sub>__._ (7.3)

Standard GARCH models assume that the log-return process has a variance (and consequently a drift) that is time-varying

_rt_+1 = _µt_+1 _−_ _ht_+1 + q_ht_+1_εt_+1_,_ (7.4)

where the variance process _<sub>ht</sub>_<sub>+1</sub> is a function of the past realizations of _<sub>hs</sub>_, _<sub>εs</sub>_, _<sub>s</sub> ≤ <sub>t</sub>_ and a set of parameters Θ.<sup>2</sup> It is important to notice that the variance process _<sub>ht</sub>_<sub>+1</sub> is time _<sub>t</sub>_\-measurable and so is _<sub>µt</sub>_<sub>+1</sub>, which usually links the one-period ahead UA premium to the variance over the same period. Hence, the mean and the variance of the next period return are known as a function of past returns. This property greatly simplifies the implementation of GARCH models.

#### 7.2.1 Nonaffine GARCH(1,1)

The GARCH class of model nests a vast array of models. Different variants imply different properties and forecasts for the variance process. Building on BMS, equation (7.4) already restricts us, for instance, to conditionally normal GARCH models. The literature abounds with models that feature nonnormal innovations in lieu of the normal _<sub>ε</sub>_ above. We will, however, focus on conditionally normal models.<sup>3</sup>

The variance transition equation itself can be expressed in countless ways. The standard GARCH(_<sub>p,q</sub>_) formulation is as follows:

_q p_

_ht_+1 = _ω_ \+ X _αkht_+1_−kε_2_t_+1_−k_ \+ X_βjht_+1_−j._ (7.5)

_k_\=1 _j_\=1

We will restrict our attention to the GARCH(1,1) family, as did much of the early GARCH option-valuation literature.

|     |     |
| --- | --- |
| _rt_+1 = _rf_ \+ _λ ht_+1 _−_ 21_ht_+1 + _ht_+1_εt_+1_,_ q q | (7.6) |
| _h<sub>t</sub>_<sub>+1</sub> \= _ω_ \+ _αh<sub>t</sub>_ (_ε<sub>t</sub> − γ_)<sup>2</sup> \+ _βh<sub>t</sub>,_ | (7.7) |

In particular, we will consider the nonaffine GARCH (NGARCH) model of Engle and Ng (1993), which assumes the following dynamics:<sup>4</sup>

where the parameter set is Θ = _{<sub>λ,α,β,γ,ω</sub>}_ and _<sub>rf</sub>_ denotes the risk-free rate. Duan (1995) uses this model for option valuation.

Note that this specification implies that _<sub>µt</sub>_<sub>+1</sub> \= _<sub>rf</sub>_ \+ _<sub>λ</sub>_<sup>p</sup>_<sub>ht</sub>_<sub>+1</sub>. Put differently, in the NGARCH model as in BMS the price of risk, the market price of risk is constant:

_µt_p+1_ht−_+1_rf_ \= _λ._

The _<sub>λ</sub>_ parameter is defined depending of the period length (typically daily). To get the annualized Sharpe ratio, we need to compute

_µt_<sub>+1</sub>p_/δ − r<sub>f</sub>/δ_ \= _~~√~~λ ._

_h_

_t_

+1

_/δ_

_δ_

<sup>2</sup>Note that _h<sub>t</sub>_ is expressed in terms of the chosen observation frequency, i.e. if _δ_ \= 1_/_252, _h<sub>t</sub>_ will be the daily variance (not annualized) of the log-returns.

<sup>3</sup>It is important to note that, at relevant pricing horizons _T_, heteroscedasticity will generally induce nonnormal cumulative log-returns.

<sup>4</sup>“Nonaffine” here highlights the fact that the moments of the variance process are not affine. Whereas this is true for most other GARCH models, we will reserve the NGARCH acronym for this particular specification.

Equation (7.7) further adds a parameter, _<sub>γ</sub>_, to the generic equation (7.5). This parameter, often referred to as the _leverage_ parameter, allows for an asymmetric response to positive and negative shocks. For _<sub>γ ></sub>_ 0, this ensures that negative returns are associated with greater increases in variance than positive returns of the same magnitude. This feature allows the model to capture a negative correlation between the underlying returns and the level of the variance. This is a desirable property when the options written on the underlying display an asymmetric volatility smile (i.e., a smirk).

#### 7.2.2 Properties of the model

In the NGARCH, the unconditional variance is given by

_σ_2 = E \[_ht_+1\]

\= _ω_ \+ _α_E <sup>h</sup>_h<sub>t</sub>_(_ε<sub>t</sub> − γ_)<sup>2i</sup> \+ _β_ E \[_h<sub>t</sub>_\]_._

Using the independence between _<sub>ht</sub>_ and _<sub>εt</sub>_, we have

_σ_<sup>2</sup> \= _._

In order to better understand the dynamics of the NGARCH(1,1) process, let us rewrite the variance equation

_h<sub>t</sub>_<sub>+1</sub> \= _σ_<sup>2</sup> 1 _− α_(1 + _γ_<sup>2</sup>) _− β_ \+ _αh<sub>t</sub>_(_ε<sub>t</sub> − γ_)<sup>2</sup> \+ _βh<sub>t</sub>,_

or, equivalently,

_ht_+1 _− σ_2 = _π ht − σ_2 + _αht εt_2 _−_ 1 _−_ 2_γεt,_ (7.8)

where _<sub>π</sub>_ \= _<sub>α</sub>_(1 + _<sub>γ</sub>_<sup>2</sup>) + _<sub>β</sub>_. Interestingly, in equation (7.8), _<sub>α</sub>_ multiplies a zero-mean innovation. Hence, taking time _<sub>t −</sub>_ 1 conditional expectation, we have

E_t−_1 h_ht_+1 _− σ_2i = _π ht − σ_2_._

This equation highlights the mean-reverting property of the variance process, as long a _<sub>π <</sub>_ 1\. Actually, it is crucial to have _<sub>π <</sub>_ 1 to ensure the stationarity of the variance process.<sup><sup>[\[7\]](#footnote-7)</sup></sup> To illustrate this point, consider the term structure of the expected conditional variances, which can be obtained by nesting the conditional expectations:

E_t−_1 h_ht_+_k − σ_2i = E_t−_1 hE_t_+_k−_2 h_ht_+_k − σ_2ii

\= _π_ E_t−_1 h_ht_+_k−_1 _− σ_2i = _..._ \= _πk ht − σ_2_._

Hence, if _<sub>π ></sub>_ 1, the process would potentially diverge. The closer _<sub>π</sub>_ is to 1, the longer a deviation from unconditional variance will persist. Thus, _<sub>π</sub>_ is referred to as the _persistence_ of the variance process. A process with a low (high) persistence will mean-revert quickly (slowly) to _<sub>σ</sub>_<sup>2</sup>.

#### 7.2.3 Other GARCH models

##### The AGARCH model

The affine GARCH model of Heston and Nandi (2000) assumes that

q

_rt_+1 = _rf_ \+ _λht_+1 _−ht_+1 + _ht_+1_εt_+1_, ht_+1 = _ω_ \+ _αεt − γ_p_ht_2 + _βht._

According to this specification, we have _<sub>µt</sub>_<sub>+1</sub> \= _<sub>rf</sub>_ \+ _<sub>λht</sub>_<sub>+1</sub>.<sup><sup>[\[8\]](#footnote-8)</sup></sup>

In the AGARCH model, the conditional Sharpe ratio is a function of the level of the conditional

volatility

_µt_p+1_ht−_+1_rf_ \= _λ_q_ht_+1_._

Again, the _<sub>γ</sub>_ parameter captures the asymmetry of the variance process. Christoffersen et al. (2010) further compare the properties of the NGARCH and AGARCH models.

The main motivation behind this specific variant of the GARCH pricing model is that, being an affine model, it allows for a quasi-analytical solution for the price of European options. Whereas this allows for tremendous computational gains, it unfortunately comes at a cost. Hsieh and Ritchken (2005) and Christoffersen et al. (2010) find that nonaffine models better fit underlying returns and option prices than their affine counterpart.

##### Other nonaffine variants

The GARCH family of models has many representatives. Here we cite some classical specifications of other GARCH models. These models, just like the NGARCH model, do not offer analytical option pricing formula and have to be solved using Monte Carlo simulation or tree methods. Amin and Ng (1993), Duan (1995), Duan and Simonato (1998) or Ritchken and Trevor (1999) develop some efficient algorithms for some GARCH models. Duan et al. (2004) use an Edgeworth expansion ot obtains analytical approximations of option price formula for GJR-GARCH and EGARCH models.

Glosten et al. (1993) propose a GARCH model, known as the GJR-GARCH model, which has the

following form

_rt_+1 = _µt_+1 _−_ 21_ht_+1 + q_ht_+1_εt_+1_,_

with

_h<sub>t</sub>_<sub>+1</sub> \= _ω_ \+ (_α_ \+ _γI<sub>t</sub>_)_h<sub>t</sub>ε_<sup>2</sup>_<sub>t</sub>_ \+ _βh<sub>t</sub>,_

with _I<sub>t</sub>_ \= 1_{ε<sub>t</sub> <_ 0_}_.

Nelson (1991) introduces the exponential form of the GARCH model named EGARCH model. The dynamics of the variance process in this model is given by

ln_h<sub>t</sub>_<sub>+1</sub> \= _ω_ \+ _α_(_|ε<sub>t</sub>|_ \+ _γε<sub>t</sub>_) + _β_ ln_h<sub>t</sub>._

While the parameters of the GJR-GARCH model should be positive to ensure a positive conditional variance, the EGARCH model does not require such restrictions.

Ding et al. (1993) and Hentschel (1995) propose a set of models capturing the asymmetry effect as well as a “news” effect at each time, the innovation is translated using a perturbation parameter. Christoffersen and Jacobs (2004) investigate which model feature is the most important and find that to be the asymmetry effect (NGARCH). They also find that there are some benefits in using parsimonious models.

#### 7.2.4 Parameter estimation

The estimation is typically performed using the maximum likelihood method based on return data only. It consists in finding the set of parameters that maximizes the likelihood that the observed historical returns have been generated by the model.

For this exercice, we use the daily log-returns _<sub>r</sub>_<sub>1</sub>_<sub>,...,rT</sub>_ computed using past realizations of the underlying price. Using a GARCH model, these returns satisfy

_rt_ \= _mt_ \+ p_htεt._

Thus, for a given set of parameters Θ, the realizations of the Gaussian innovations write as

_εt_ (Θ) = _rt_p_− mt_ (Θ)_, h<sub>t</sub>_ (Θ)

for all times _<sub>t</sub>_ \= 1_<sub>,...T</sub>_ and where _<sub>mt</sub>_ (Θ) and _<sub>ht</sub>_ (Θ) depend on the GARCH model considered. In order to compute these innovations, we need to iterate starting from date 1. Without loss of generality, we can set

_h_1 = _V ar {rt}t_\=1_,...T ,_

that is, the first estimate of the date 1 variance is simply the historical sample variance. Alternatively, one can also simply start with _<sub>h</sub>_<sub>1</sub> \= _<sub>r</sub>_<sub>1</sub><sup>2</sup>.

The probability density function of _<sub>rt</sub>_ conditional on time _<sub>t −</sub>_ 1 is then given by

_._

So the joint probability density of the vector of _<sub>T</sub>_ observations (i.e., the total likelihood), assuming the same order of observations, is

_._

_t_

Note that in fact these observations are not independent due to the autocorrelation of the _<sub>ht</sub>_ process.

For our model to be consistent with the empirical data, the volatility dynamics should be such that this probability is maximized. Thus, estimation of the variance dynamics is obtained by maximizing the log-likelihood function, that is,

Θ_<sup>∗</sup>_ \= argmax _<sub>−</sub>_ <sup>1 X</sup>_<sup>T</sup>_ ln2_π_ \+ ln_h<sub>t</sub>_ (Θ) + _ε_<sup>2</sup>_<sub>t</sub>_ (Θ)<sup>!</sup>_._

Θ 2 _t_\=1

This type of optimization leads to several local extremums in general. It is thus recommended to provide more details for the search of the optimal solution by imposing constraints on the parameters such as imposing the stationarity property of variance.

#### 7.2.5 Risk-neutralization

##### General principle

Since the parameters are obtained using the historical returns on the underlying, the GARCH model is estimated under the physical measure. In order to value derivatives, one must first adjust the model to obtain its risk-neutral dynamics. To this end, Duan (1995) develops a methodology called the local riskneutral valuation relationship (LRNVR). Similarly to the Girsanov theorem in continuous time, the idea of this local risk-neutral valuation is used to translate the Gaussian innovations in such a way that the underlying returns under Q equal the risk-free rate. Hence, the GARCH model writes as follows under Q

_rt_ p_htε∗t ,_

where _<sub>t</sub>_ and _<sub>ηt</sub>_ denote the adjustment process towards the EMM measure. Equalizing the two dynamics, we obtain

_µt_ p_ht_p_htε∗t ,_

and hence

_ηt_ \= _µt~~√~~− rf ._

_h<sub>t</sub>_

In other words, the adjustment process _<sub>ηt</sub>_ needs to equate the market price of risk (similarly to the RadonNikodym derivative in the Girsanov theorem when dealing with continuous time processes).

##### Applications

|     |     |     |
| --- | --- | --- |
| _rt_+1 | \=  | _rf_ \+ _λ ht_+1 _−_ 21_ht_+1 + _ht_+1_εt_+1_,_ q q |
| _ht_+1 | \=  | _ω_ \+ _αh<sub>t</sub>_ (_ε<sub>t</sub> − γ_)<sup>2</sup> \+ _βh<sub>t</sub>._ |

Let us reconsider the NGARCH model. The P dynamics is given by

To switch to the Q measure, we need to translate the Gaussian innovation by the market price of risk, which in this model is given by _<sub>√</sub>_

_η<sub>t</sub>_ \= _rf_ \+ _λ√ ht − rf_ \= _λ._

_h<sub>t</sub>_

So, under Q, we have

q

_rt_+1_ht, h<sub>t</sub>βh<sub>t</sub>,_

hence finally

 = _rf_q_ht_+1_ε∗<sub>t</sub>_<sub>+1</sub>_,_

_rt_+1

_ht_+1 = _ω_ \+ _αht._

where _<sub>γ</sub><sup>∗</sup>_ \= _<sub>γ</sub>_+_<sub>λ</sub>_. It appears that under Q, the NGARCH model keeps the same properties at the exception that the expectation of the underlying returns is the risk-free rate and the asymmetry parameter becomes _λ_+_<sub>γ</sub>_, which accentuates (whenever _<sub>λ ></sub>_ 0) the negative correlation between returns and volatility. For the

AGARCH model, the market price of risk is given by

q

_ηt_ \= _λ ht_+1_,_

and hence the Q dynamics become

q q _rt_+1 = _rfhtht_+1 _,_

 2 _ht_p_ht − γ_p_ht_ \+ _βht,_

which yields

q_∗_

_h_

_t_

+1

_rt_+1_ε<sub>t</sub>_<sub>+1</sub>_, ht_p_ht_2 + _βht._

Once again, the AGARCH model keeps the same properties under the Q measure at the exception that the expected value of the returns is the risk-free rate and that the asymmetry parameter becomes _<sub>γ</sub>_ \+ _<sub>λ</sub>_, which once again accentuates the negative correlation between returns and volatility.

**7.3 Stochastic volatility models**

This family of models is a natural extension of the GARCH models since Nelson (1990) shows that several GARCH models converge in continuous time to a diffusion process for the variance. Hull and White (1987) show that, when the underlying returns and its variance are not correlated, the value of the option equals the average of the option values obtained using the BMS model, with the average being computed over the distribution of the variances _<sub>f</sub>_. Hence, we have

Z _∞_

_g_ \= _g<sub>BMS</sub>_ (_v_)_f_ (_v_)_dv,_

0

where _<sub>v</sub>_ denotes the variance of the underlying returns. Note, however, that Nandi (1998) demonstrates the importance of incorporating a correlation (usually negative) between the returns of the underlying and the variance process.

Hull and White (1987) study the general case where the dynamics of the underlying returns variance is given by

_dv<sub>t</sub>_ \= _κσ_<sup>2</sup> _− v<sub>t</sub>dt_ \+ _αv<sub>t</sub><sup>θ</sup>dZ_ (_t_) (7.9)

where _<sub>κ</sub>_, _<sub>σ</sub>_<sup>2</sup>, _<sub>α</sub>_ and _<sub>θ</sub>_ are four positive constants. This specification takes into account the mean-reverting property of the volatility. Generally speaking, one needs to resort to numerical methods to compute _<sub>g</sub>_. Some special cases have been deeply studied in the literature. Before reviewing these cases, it is important to emphasize that the introduction of an additional source of risk alters the arbitrage argument in the BMS model and consequently the valuation of options. We now study in more details this point (see in particular Wiggins (1987)).

#### 7.3.1 Hedging in the presence of stochastic volatility

Here our aim is to value a derivative _<sub>g</sub>_ and we assume the following functional form

_g_ \= _g_ (_S<sub>t</sub>,v<sub>t</sub>,t_)_._

Assume that the UA price is driven by a geometric Brownian motion with drift _<sub>µ</sub>_ and volatility _<sup>√</sup><sub>vt</sub>_, where _v<sub>t</sub>_ satistifies the generic Hull and White (1987) stochastic differential equation.

Consider the portfolio _<sub>P</sub>_ consisting of _<sub>n</sub>_<sub>1</sub> units of _<sub>g</sub>_ and _<sub>n</sub>_<sub>2</sub> units of the UA

_P_ \= _n_<sub>1</sub>_g_ \+ _n_<sub>2</sub>_S._

Assuming this portfolio is self-financed, the change in its value over a short time period is given by Itˆo’s

lemma = \[_n_<sub>1</sub> (_g<sub>t</sub>_ \+ _A_(_g_)) + _n_<sub>2</sub>_µS_\]_dt_ \+ _<sub>√</sub>vS_ (_n_<sub>1</sub>_g<sub>S</sub>_ \+ _n_<sub>2</sub>)_dW_ \+ _n_<sub>1</sub>_αvθg<sub>v</sub>dZ, dP_

with

 _A_(_g_) = _µSg<sub>S</sub>_ \+ _κσ_<sup>2</sup> _− vg<sub>v</sub>_ _vSαv<sup>θ</sup>g<sub>Sv</sub>,_

where _<sub>ρ</sub>_ is the correlation coefficient between the two Brownian motions and where the indices denote the partial derivatives (the _<sub>A</sub>_ operator is known as the infinetesimal generator).

Note that, in contrast to the BMS case, we cannot hedge the portfolio against the two sources of risk since we have only the UA and the risk-free asset at hand to replicate the derivative _<sub>g</sub>_. The market is said to be incomplete as perfect hedging is not feasible.

Since we cannot construct a risk-free portfolio, we will focus on a particular position, namely the one that has zero correlation with the UA. We call this a zero-beta portfolio. It can be obtained by setting _dPdS_ \= 0_,_

which yields <sup>2</sup> (_n_<sub>1</sub>_g<sub>S</sub>_ \+ _n_<sub>2</sub>)_dt_ \+ _n_<sub>1</sub>_αv √vSg<sub>v</sub>ρdt,_ 0 = _vS θ_

or equivalently

_θ_ !

_ραv n_<sub>2</sub> \= _− g<sub>S</sub>_ \+ _~~√~~ g<sub>v</sub> n_<sub>1</sub>_. vS_

The zero-beta portfolio becomes

_dP_ \= _n_<sub>1</sub> _g<sub>t</sub>_ \+ _A_(_g_) _− µSg<sub>S</sub> − <sup>ρµα</sup>~~√~~ v<sup>θ</sup>g<sub>v</sub>dt_ \+ _n_<sub>1</sub>_αv<sup>θ</sup>g<sub>v</sub>_ (_dZ − ρdW_)_. v_

The portfolio expected return _<sub>µ</sub><sup>P</sup>_ is given by

_µ<sup>P</sup> Pdt_ \= E \[_dP_\]

\= _n_1 _gt_ \+ _A_(_g_) _− µSgS − ρµα~~√~~ vθgvdt v_

and the return volatility _<sub>σ</sub><sup>P</sup>_ is

_σP P_2 _dt_ \= E h(_<sub>dP</sub>_)2i

\= _n_1_αvθgv_2 1 _− ρ_2_dt,_

or

_σ<sup>P</sup> P_ \= _±n_<sub>1</sub>_αv<sup>θ</sup>g<sub>v</sub>_<sup>q</sup>(1 _− ρ_<sup>2</sup>)_,_

since _<sub>α</sub>_ is positive and _<sub>gv</sub>_ is positive for most of derivatives. Let us now introduce the ratios of market prices of risk

_λP_ \= _µPσP− r_ and _λ_ \= _µ~~√~~−vr._

By construction, _<sub>λ</sub><sup>P</sup>_ is the market price of volatility risk (since the zero-beta portfolio is hedged against the UA price risk), and _<sub>λ</sub>_ is the market price of risk of the UA. We can rewrite

_µ<sup>P</sup> P − rP_ \= _Pλ<sup>P</sup> σ<sup>P</sup> ,_

which yields, after some simplifications,

 + _ραv g<sub>v</sub>_q(1 _− ρ_<sup>2</sup>)_λ<sub>P</sub> ._

_g<sub>t</sub>vSg<sub>S</sub>_

**Proposition 7.1** _In the presence of stochastic volatility satisfying dv<sub>t</sub>_ \= _κ σ_<sup>2</sup> _− v<sub>t</sub>dt_ \+ _αv<sub>t</sub><sup>θ</sup>dZ_ (_t_)_, every derivative should satisfy the PDE_

_g<sub>t</sub>_ \+ _A_<sub>2</sub> (_g_) = _rg,_

_where_

_A_2 (_g_) = _rSgS_  _P gv_

 _vSαv<sup>θ</sup>g<sub>Sv</sub>. This PDE has to be solved with the appropriate terminal conditions._

This proposition characterizes the no arbitrage connection between the dynamics under the physical measure (P) and those under the EMM (Q). Indeed, from the Feynman-Kac theorem, the derivative _<sub>g</sub>_ must satisfy the PDE _<sub>gt</sub>_ \+ _<sub>A</sub>_<sub>2</sub> (_<sub>g</sub>_) = _<sub>rg</sub>_ where the infinitesimal generator _<sub>A</sub>_<sub>2</sub> (_<sub>g</sub>_) contains EMM drifts (associated with first-order partial derivatives), EMM volatility functions (associated with second-order partial derivatives), and EMM correlation function (associated with the second-order cross derivative).

Consequently, the proposition indicates that the generic Hull and White (1987) stochastic volatility model is subject to the following changes when shifting from P to Q:

1\. the drift of the UA becomes the risk-free rate, 2. the drift of volatility becomes

_κσ_2 _− v_ _− αvθ λρ ±_ q(1 _− ρ_2)_λP ,_

3\. the correlation coefficient _<sub>ρ</sub>_ and all diffusion coefficients remain the same.

#### 7.3.2 Some special cases

##### Hull and White (1987)

As we already mentioned, the special case _<sub>θ</sub>_ \= 1 corresponds to the continuous time limit of a GARCH process. This model is referred to a diffusion GARCH.

In the very special case where _<sub>κ</sub>_ \= 0 and _<sub>θ</sub>_ \= 1, the variance follows a geometric Brownian motion without drift. If, in addition, _<sub>ρ</sub>_ \= 0, Hull and White (1987) obtain a closed-form formula using a Taylor expansion

_c<sub>HW</sub>_ (_S,v,α,T_)

_√_

\= _cBMS v_

 

\+ _− α_2

+6 8_v_5_<sub>/</sub>_<sub>2</sub>

_e_!

_×v_3_,_

3_α_6_T_3

where _<sub>d</sub>_<sub>1</sub> and _<sub>d</sub>_<sub>2</sub> have the same definitions as in the BMS model.

##### Heston (1993)

Heston (1993) introduces and studies the case of _<sub>θ</sub>_ \= 1_<sub>/</sub>_2, arguably the most famous member of the stochastic volatility family of models.<sup><sup>[\[9\]](#footnote-9)</sup></sup> This model assumes the following dynamics under the historical probability

_√_

_dS<sub>t</sub>_ \= _µS<sub>t</sub>dt_ \+ _v<sub>t</sub>S<sub>t</sub>dW<sub>t</sub>_

_dv<sub>t</sub>_  _v<sub>t</sub>dt_ \+ _α√v<sub>t</sub>dZ<sub>t</sub>,_

where

_dW<sub>t</sub>dZ<sub>t</sub>_ \= _ρdt._

Importantly, Heston (1993) also assumes that the total market price of volatility risk has the specification _λ_(_<sub>S,v,t</sub>_) = _<sub>λv</sub>_ where _<sub>λ</sub>_ is a constant.

The risk-neutral dynamics are therefore given by

_√_

_dS<sub>t</sub>_ \= _rS<sub>t</sub>dt_ \+ _v<sub>t</sub>S<sub>t</sub>dW<sub>t</sub>_

 i _√_

_dv<sub>t</sub>λv<sub>t</sub> dt_ \+ _α v<sub>t</sub>dZ<sub>t</sub>,_

or, equivalently

|     |     |     |
| --- | --- | --- |
| _dS<sub>t</sub>_ | \=  | _√_<br><br>_rS<sub>t</sub>dt_ \+ _v<sub>t</sub>S<sub>t</sub>dW<sub>t</sub>_ |
| _dv<sub>t</sub>_ | \=  | <sup>h 2</sup> _−_ (_κ_ \+ _λ_)_v<sub>t</sub>_<sup>i</sup>_dt_ \+ _α<sup>√</sup>v<sub>t</sub>dZ<sub>t</sub>._<br><br>_κσ_ |

Assuming the AoA, the value of the European call option is given by

_c_(0_,T,K_) = _SP_<sub>1</sub> _− Ke<sup>−rT</sup> P_<sub>2</sub>_,_

with

_Pj_ \= 12 + _π_1 Z0_∞_ Re _e−iϕ_ln(_K_)_fiϕj_ (_S,v,T,ϕ_)!_dϕ,j_ \= 1_,_2_,_

and

_f<sub>j</sub>_ (_S,v,T,ϕ_) = exp\[_C<sub>j</sub>_ (_T,ϕ_) + _D<sub>j</sub>_ (_T,ϕ_)_v_ \+ _iϕ_ln(_S_)\]_,j_ \= 1_,_2_,_

where

_Cj_ (_T,ϕ_) = _rϕiT_ \+ _κσα_22 ((_bj − ραϕi_ \+ _dj_)_T −_ 2ln 1 _−_1 _−gjegdjjT_ !)_,j_ \= 1_,_2_,_

_D_ (_T,ϕ_) = _bj − ραϕi_ \+ _dj_ 1 _− edjT_ !_,j_ \= 1_,_2_,_

1 _− g e_

_j_

_α_

2

_j_

_d_

_j_

_T_

with

\= _b<sup>j</sup> − ραϕi_ \+ _d<sup>j</sup>_

_gj <sub>,j</sub>_ \= 1_<sub>,</sub>_2_<sub>,</sub>_

_b<sub>j</sub> − ραϕi − d_

_j_

_d<sub>j</sub>_ \= <sup>q</sup>(_ραϕi − b<sub>j</sub>_)<sup>2</sup> _− α_<sup>2</sup> (2_u<sub>j</sub>ϕi − ϕ_<sup>2</sup>)_,j_ \= 1_,_2_,_

_u_1 = 12 _u_2 = _−_12 _b_<sub>1</sub> \= _κ_ \+ _λ − ρα b_<sub>2</sub> \= _κ_ \+ _λ_

The Heston (1993) model is flexible enough to generate different forms of the volatility smiles. In particular, when the correlation coefficient (_<sub>ρ</sub>_) is null, the smile is symmetric. When _<sub>ρ</sub>_ is negative (positive), the smile is decreasing (increasing).

To simulate the model, one needs to define a discretization scheme. Lord et al. (2010) study the following Euler discretization schemes

_vt_+∆_t tε,_

\=

_f_

1

(

_v_

_t_

)+

_κ_

_σ_

2

_−_

_f_

2

(

_v_

_t_

)

∆

_t_

+

_α_

q

_f_

3

(

_v_

_t_

)

_√_

∆

with

###### Scheme _f_<sub>1</sub> (_x_) _f_<sub>2</sub> (_x_) _f_<sub>3</sub> (_x_)

|     |     |     |     |
| --- | --- | --- | --- |
| 1   | _x_+ | _x_+ | _x_+ |
| 2   | _\|x\|_ | _\|x\|_ | _\|x\|_ |
| 3   | _x_ | _x_ | _\|x\|_ |
| 4   | _x_ | _x_ | _x_+ |
| 5   | _x_ | _x_+ | _x_+ |

where _<sub>x</sub>_<sup>\+</sup> denotes the positive part of _<sub>x</sub>_. The authors show that, among the five schemes, the one that produces the best results is the fifth (known as the _full truncation scheme_). This scheme allows _<sub>vt</sub>_ to pick temporarily some negative values. Whenever this occurs, the variance dynamics becomes deterministic _v<sub>t</sub>_<sub>+∆</sub>_<sub>t</sub>_ \= _<sub>κσ</sub>_<sup>2</sup>∆_<sub>t</sub>_ until the variance picks positive values. Non-Euler schemes are proposed by Kahl and J¨ackel (2006) or Broadie and Kaya (2006).

Several empirical studies including Gesser and Poncet (1997) on the exchange rate market and Dragulescu and Yakovenko (2002) and Shu and Zhang (2004) on indices confirm the superiority of the Heston (1993) model over the constant volatility BMS model.

##### The SABR model

This model has been proposed by Hagan et al. (2002). The SABR acronym stands for _Stochastic Alpha, Beta and Rho_. Indeed, the model has only three parameters, since its applies directly to the dynamics of the forward price. This dynamics is given by

_dFt_ \= _σtFtβdWt,_

_dσ<sub>t</sub>_ \= _ασ<sub>t</sub>dZ<sub>t</sub>,_

with

_dW<sub>t</sub>dZ<sub>t</sub>_ \= _ρdt._

A rather good approximation of the European call premium can be obtained by inserting the following implied volatility in the Black (1976) formula (this result is based on a Taylor expansion)

_σimp_ \= _αD_ln(_<sub>ξ</sub>KF_) 1 + <sub></sub>2_γ_2 _− γ_1224+ 1_/Fmid_2 _σtFαmidβ_ !2 + _ργ_41 _σtFαmidβ_ \+ 2 _−_243_ρ_2 _Tα_2_,_

with

_αF_1_−β − K_1_−β_ _ξ_ \=_,_

_σ_ (1 _− β_)

_t_

_β_

_,_

_γ_<sub>1</sub> \=

_Fmid_

_γ_<sub>2</sub> \= _−β_ (12_− β_)_,_

_Fmid_

 2 !

_D_ (_<sub>ξ</sub>_) = ln_<sub>,</sub>_

and _<sub>Fmid</sub>_ is the forward price at half way between_√_ _F_ and _<sub>K</sub>_. In practice, one can use an arithmetic average ((_<sub>F</sub>_ \+ _<sub>K</sub>_)_<sub>/</sub>_2) or a geometric one _<sub>FK</sub>_ .

**7.4 CEV models**

The acronym CEV is short for Constant Elasticity of Variance. It denotes a family of models in which the risk-neutral dynamics of the underlying has the following form:

_dS<sub>t</sub>_ \= (_r − y_)_S<sub>t</sub>dt_ \+ _σS<sub>t</sub><sup>β</sup>_<sup>2</sup> _dW<sub>t</sub>,_

with _<sub>β <</sub>_ 2\. Cox and Ross (1976) study the particular case _<sub>β</sub>_ \= 1, i.e. SRCEV model (Square Root Constant Elasticity of Variance). Beckers (1980) and Schr¨oder (1989) study other representative models of this family. Cox (1996) reconsidering some 1975 notes proposes a solution to the general case. More recently, Hui et al. (2000) examine the model when the parameters _<sub>r</sub>_ and _<sub>σ</sub>_ are deterministic functions of time.

The CEV models include the geometric Brownian motion (_<sub>β</sub>_ \= 2), the square root process (_<sub>β</sub>_ \= 1) and the Ornstein-Uhlenbeck process (_<sub>β</sub>_ \= 0). Note that the return variance is _<sub>σ</sub>_<sup>2</sup>_<sub>S</sub><sup>β−</sup>_<sup>2</sup>. Hence CEV models typically generate asymmetric implied volatility smiles since the level of return variance is inversely related to the level of the UA price. That is why authors like Schmalensee and Trippi (1978) and Hauser and Lauterbach (1996) have applied these models to describe the dynamics of stock prices. Furthermore, we have

_dv/dS_

\= _β −_ 2_. v/S_

Thus, we can interpret _<sub>β −</sub>_ 2 as the elasticity of the return variance (which explains the CEV acronym). Several pricing formulas have been proposed for the valuation of European options. Arguably, the most easily tractable is the one involving the chi squared distribution (see Cox, 1996)

_c_(0_,T,K_) = _Se−yT_ 1 _− Q_2_a_;2 + _,_2_x_ _− Ke−rT Q_2_x_; _,_2_a,_

with

_a_ \= _kK_2_−β,_

_<sub>x</sub>_ \= _<sub>kS</sub>_2_−β<sub>e</sub>_(_r−y_)(2_−β_)_T <sub>,</sub> k_ \= _σ_2 (2 _− β_)2(_er_(_r−−yy_)(2)_−β_)_T −_ 1_,_

and _<sub>Q</sub>_(_<sub>z</sub>_;_<sub>v,λ</sub>_) is the cumulative distribution function of the non-centered chi squared distribution with _<sub>v</sub>_ degrees of freedom and non-centrality parameter _<sub>λ</sub>_ evaluated at _<sub>z</sub>_.

**7.5 Problem set**

#### Exercise 7.1

One of the simplest GARCH models is the GARCH(1,1) model:

_r<sub>t</sub>_+1 = <sup>q</sup>_h<sub>t</sub>_+1_ε<sub>t</sub>_+1_, ht_+1 = _ω_ \+ _αrt_2 + _βht._

Whereas this simple version of the model is useful in many applications, it has serious limitations in an option-valuation context.

1.  What is the implicit _<sub>µt</sub>_<sub>+1</sub> assumed here? What does it imply for the market price of risk in this model? How is that problematic?
2.  Show that the transition equation for the variance process is a nested case of the NGARCH model.
3.  You decide to use a GARCH(1,1) anyway. The estimation of the model based on weekly returns yields

_h<sub>t</sub>_<sub>+1</sub> \= 0_._4_h<sub>t</sub>_ \+ 0_._15_r<sub>t</sub>_<sup>2</sup> \+ 0_._001_._

What is the long term weekly variance of the underlying returns?

1.  On week _<sub>t</sub>_, the weekly variance of the underlying filtered during estimation is _<sub>ht</sub>_<sub>+1</sub> \= 0_<sub>.</sub>_0012\. For an arbitrary week _<sub>t</sub>_ \+ _<sub>k</sub>_, compute the time _<sub>t</sub>_ \+ _<sub>k</sub>_ expectation of the variance.
2.  Rather than using simulations to price a given option, you decide to simply to use BMS, but with the expected volatility over the life of the said option. The derivative has four weeks to expiration.

Which volatility should we use in the BMS formula to value this derivative?

#### Exercise 7.2

1.  Show that the persistence of the variance process of the NGARCH model is _<sub>α</sub>_ 1 + _<sub>γ</sub>_<sup>2</sup> \+ _<sub>β</sub>_, and the unconditional variance is given by _<sub>ω/</sub>_ 1 _− <sub>α</sub>_ 1 + _<sub>γ</sub>_<sup>2</sup> _− <sub>β</sub>_.
2.  Similarly, show that the variance persistence of the AGARCH model is _<sub>αγ</sub>_<sup>2</sup>+_<sub>β</sub>_, and the unconditional variance is given by (_ω_ \+ _α_)_/_ 1 _− <sub>αγ</sub>_<sup>2</sup> _− <sub>β</sub>_.
3.  Derive, in both models, Cov<sub>t</sub> (_<sub>rt</sub>_<sub>+1</sub>_<sub>,ht</sub>_<sub>+2</sub>), the conditional covariance between future returns and variance.

#### Exercise 7.3

Consider the following component NGARCH model:

_rt_+1 = _rf_ _,_

_h<sub>t</sub>__,_

 _qt_+1_,_

where the _<sub>εt</sub>_ are standard normal innovations under P.

1.  Show that the unconditional mean of the process _<sub>qt</sub>_ is _<sub>σ</sub>_<sup>2</sup>.
2.  Derive the unconditional mean of the process _<sub>ht</sub>_.
3.  Given the information at time _<sub>t −</sub>_ 1, what is the model’s forecast of variance at _<sub>t</sub>_ \+ _<sub>k</sub>_? \[Hint: _ht_+_k_ \= _qt_+_k_ \+ (_ht_+_k − qt_+_k_)\]
4.  Given the information at time _<sub>t −</sub>_ 1, what is the variance of _<sub>ht</sub>_<sub>+1</sub>?
5.  What is the role played by _<sub>γ</sub>_<sub>1</sub> and _<sub>γ</sub>_<sub>2</sub>? Which sign do you expect these parameters to have if you estimate the model using historical S&P 500 log-returns? According to you, which one of these two parameters will be larger in magnitude (_<sub>|γ|</sub>_)?
6.  Consider a process _<sub>η</sub>_ such that

_erf_ \= E exp _µt_+1 _− ht_+1 + _ht_+1 _ε_ +1 _− ηt_+1_,∀t._

Find _<sub>ηt</sub>_ for the component NGARCH model and use it to write the risk-neutral form of the model. Compare the model under Q to that under P.

1.  After estimating the parameters of the model under P, you wish to price an option on the S&P 500, with maturity _<sub>τ</sub>_, using the above model. Explain your procedure in sufficient details.

#### Exercise 7.4

Consider a stochastic volatility model assuming the following dynamics (under the physical measure)

_dS_

_<sup>t</sup>_ \= _µ_d_t_ \+ _σ<sub>t</sub>_ d_W<sub>t</sub>,_

_S<sub>t</sub>_

_dσ<sub>t</sub>_ \= _−λσ<sub>t</sub>_ d_t_ \+ _α<sup>√</sup>σ<sub>t</sub>_ d_Z<sub>t</sub>,_

where _<sub>S</sub>_ denotes the UA price, _<sub>σt</sub>_ is the volatility process, _<sub>µ</sub>_, _<sub>λ</sub>_ and _<sub>θ</sub>_ are three positive constants, and _<sub>Wt</sub>_ and _<sub>Zt</sub>_ are two correlated Brownian motions with a correlation coefficient _<sub>ρ</sub>_.

1.  Consider a derivative written on _<sub>S</sub>_ whose value is denoted by _<sub>g</sub>_ (_<sub>S,σ,t</sub>_). Use Itˆo’s lemma to identify the dynamics of this derivative.
2.  Explain how these dynamics of _<sub>S</sub>_ and _<sub>σ</sub>_ are altered when switching to the risk-neutral measure (specify in particular the parameters which remain unchanged and those which are modified).

#### Exercise 7.5

Consider the following CEV model

d_SStt_ \= _r_d_t_ \+ _S<sub>t</sub>_1_σ−α_ d_Wt,_

where _<sub>W</sub>_ is a standard Brownian motion.

1.  Our aim is to value a derivative written on _<sub>S</sub>_ using Monte Carlo simulation. Write a simulation equation for the UA price.
2.  Describe the variance reduction technique called control variate technique.
3.  Assume we want to value a European option. Adopting a CEV model, which control variate could be used?

#### Exercise 7.6

Consider the stochastic volatility model with the following P-dynamics

d_S<sub>t</sub>_ \= _mS<sub>t</sub>_ d_t_ \+ _<sup>√</sup>v<sub>t</sub>S<sub>t</sub>_ d_W<sub>t</sub>_ d_v<sub>t</sub>_ \= (_a − bv<sub>t</sub>_) d_t_ \+ _c<sup>√</sup>v<sub>t</sub>_ d_Z<sub>t</sub>,_

where _<sub>W</sub>_ and _<sub>Z</sub>_ are two Brownian motions with correlation coefficient _<sub>d</sub>_.

1.  Under what condition(s) for which parameter(s) does the variance process follow a mean-reverting behavior?
2.  Assuming the mean-reversion condition in question a) is satisfied, what is the equilibrium value for the variance process?
3.  Which parameter(s) directly impact on the tails of the UA return distribution?
4.  Which parameter(s) directly impact on the smile asymmetry?
5.  When shifting the model dynamics to the EMM, what are the parameters that change and what are those that do not?

**7.6 Solutions**

#### Solution 7.1

(a) _<sub>µt</sub>_<sub>+1</sub> \= <sup>1</sup><sub>2</sub>_h<sub>t</sub>_<sub>+1</sub>, such that _<sub>µt</sub>_<sub>+1</sub> and the convexity correction terms cancel one another. The market price of risk in this model is thus

_µt_p+1 _t−_+1_rf_ \= 12q _t_+1 _hrt_+1 _._

_h_

_−_

_f_

p

_h_

Not only does this price of risk have a awkward-looking dynamics, but it involves no parameter allowing a fit to the actual data at hand. (b) We have

_ht_+1 = _ω_ \+ _αrt_2 + _βht_

\= _ω_ \+ _αh<sub>t</sub>ε_<sup>2</sup>_<sub>t</sub>_ \+ _βh<sub>t</sub>_ \= _ω_ \+ _αh<sub>t</sub>_ (_ε<sub>t</sub> − γ_)<sup>2</sup> \+ _βh<sub>t</sub>,_

for _<sub>γ</sub>_ \= 0.

2862, since the BMS formula relies on an

annual (12 months) volatility measure.

#### Solution 7.2

1.  In the NGARCH model, we have

_h<sub>t</sub>_<sub>+1</sub> \= _ω_ \+ _αh<sub>t</sub>_ (_ε<sub>t</sub> − γ_)<sup>2</sup> \+ _βh<sub>t</sub>._

The unconditional variance solves

_σ_<sup>2</sup> \= E \[_h<sub>t</sub>_<sub>+1</sub>\] = _ω_ \+ _ασ_<sup>2</sup> \+ _αγ_<sup>2</sup>_σ_<sup>2</sup> \+ _βσ_<sup>2</sup>_,_

which yields

_σ_<sup>2</sup> \= _._

|     |     |     |
| --- | --- | --- |
| We can now calculate |     |     |
| E h 2i _t−_1 _ht_+1 _− σ_ | \=  | E_t−_1 h_ω_ \+ _αht_ (_εt − γ_)2 + _βht − σ_2i |
|     | \=  | _ω_ \+ E_t−_1 _αhtε_2_t_ \+ _αhtγ_2 _−_ 2_αhtεtγ_ \+ _βht − σ_2i h |
|     | \=  | _ω_ \+ _α_ 1 + _γ_<sup>2</sup> \+ _βh<sub>t</sub> − σ_<sup>2</sup> |
|     | \=  | 1 + 2 + _<sub>t − σ</sub>_2_<sub>.</sub> α γ β h_ |

The variance process thus has a persitence equal to _<sub>α</sub>_ 1 + _<sub>γ</sub>_<sup>2</sup> \+ _<sub>β</sub>_.

1.  In the AGARCH model, we have

_ht_+1 = _ω_ \+ _αεt − γ_p_ht_2 + _βht._

The unconditional variance solves

_σ_2 = E \[_ht_+1\] = _ω_ \+ _α_ \+ _αγ_<sup>2</sup>_σ_<sup>2</sup> \+ _βσ_<sup>2</sup>_,_

which yields

_σ_<sup>2</sup> \=_._

|     |     |     |
| --- | --- | --- |
| We can now calculate |     |     |
| E h 2i _t−_1 _ht_+1 _− σ_ | \=  | E + _− γ_p_ht_2 + _βht − σ_2<br><br>_t−_1 _ω α ε<sub>t</sub>_ |
|     | \=  | _ω_ \+ E_t−_1 _αε_2_t_ \+ _αhtγ_2 _−_ 2_α_p_htεtγ_ \+ _βht − σ_2i h |
|     | \=  | _ω_ \+ _α_ \+ _αh<sub>t</sub>γ_<sup>2</sup> \+ _βh<sub>t</sub> − σ_<sup>2</sup> |
|     | \=  | _ω_ \+ _α_ \+ _αγ_<sup>2</sup> \+ _βh<sub>t</sub> − σ_<sup>2</sup> |
|     | \=  | 2 + _<sub>t</sub> − <sub>σ</sub>_2_<sub>.</sub> αγ β h_ |

The variance process thus has a persitence equal to _<sub>αγ</sub>_<sup>2</sup> \+ _<sub>β</sub>_.

1.  In the NGARCH model, we have

Covt (_rt_+1_,ht_+2) = Covt q_ht_+1_εt_+1_,αht_+1(_εt_2+1 _−_ 2_γεt_+1 + _γ_2)

\= _αh_3_t_+1_/_2 hCovt _εt_+1_,ε_2_t_+1 _−_ 2_γ_ Covt (_εt_+1_,εt_+1)i

\= _−_2_αγh_3_t_+1_/_2 _,_

since the first covariance on the second line is 0. To obtain the correlation, we need Var<sub>t</sub> (_<sub>rt</sub>_<sub>+1</sub>) = _<sub>ht</sub>_<sub>+1</sub> and

Vart (_ht_+2) = Vart _αht_+1(_ε_2_t_+1 _−_ 2_γεt_+1 + _γ_2)

\= _α_2_h_2_t_+1(2 + 4_γ_2)_._

Hence, Corr<sub>t</sub> (_r<sub>t</sub>_<sub>+1</sub>_,h<sub>t</sub>_<sub>+2</sub>) = _−_2_γ_ <sup>.p</sup>~~2 + 4~~_γ_<sup>2</sup> .

In the AGARCH model, we have

Covt (_rt_+1_,ht_+2) = Covt q_ht_+1_εt_+1_,α_(_ε_2_t_+1 _−_ 2_γ_q_ht_+1_εt_+1 + _γ_2_ht_+1)

\= _−_2_αγh<sub>t</sub>_<sub>+1</sub>_,_

To obtain the correlation, we need Var<sub>t</sub> (_<sub>rt</sub>_<sub>+1</sub>) = _<sub>ht</sub>_<sub>+1</sub> and

Vart (_ht_+2) = Vart _α_(_ε_2_t_+1 _−_ 2_γ_q_ht_+1_εt_+1 + _γ_2_ht_+1)

\= _α_<sup>2</sup>(2 + 4_γ_<sup>2</sup>_h<sub>t</sub>_<sub>+1</sub>)_._

Hence, Corr<sub>t</sub> (_r<sub>t</sub>_<sub>+1</sub>_,h<sub>t</sub>_<sub>+2</sub>) = _−_2_γ_<sup>p</sup>_h<sub>t</sub>_<sub>+1</sub> <sup>.p</sup>2 + 4_γ_<sup>2</sup>_h<sub>t</sub>_<sub>+1</sub> . As noted by Christoffersen et al. (2010), this correlation is time-varying as opposed to the above.

#### Solution 7.3

1.  We have
    1.  \[_qt_+1\] = _σ_2 + _α_2 E \[_ht_\]E h_ε_2_t −_ 1i + _β_2 E \[_qt_\] _− σ_2_,_

\= _σ_2 + _β_2 E \[_qt_\] _− σ_2_._

Hence the unconditional mean E \[_<sub>q•</sub>_\] is such that

- - 1.  _− β_<sub>2</sub>)E \[_q<sub>•</sub>_\] = (1 _− β_<sub>2</sub>)_σ_<sup>2</sup> E \[_q<sub>•</sub>_\] = _σ_<sup>2</sup>_._

1.  Similarly,
    1.  \[_ht_+1\] = E \[_qt_+1\] + _α_1 E \[_ht_\]E h_ε_2_t −_ 1i + _β_1 E \[_ht − qt_\]

\= _σ_2 + _β_1 E h_ht − σ_2i_._

So the unconditional mean E \[_<sub>h•</sub>_\] is such that

- - 1.  _− β_<sub>1</sub>)E \[_h<sub>•</sub>_\] = (1 _− β_<sub>1</sub>)_σ_<sup>2</sup> E \[_h<sub>•</sub>_\] = _σ_<sup>2</sup>_._

1.  First, we have

E_t−_1 \[_qt_+1\] = _σ_2 + _α_2 E_t−_1 \[_ht_\]E_t−_1 h_ε_2_t −_ 1i + _β_2 E_t−_1 \[_qt_\] _− σ_2

\= _σ_2 + _β_2 _qt − σ_2_,_

and, by induction,

E_t−_1 \[_qt_+_k_\] = _σ_2 + _β_2_k qt − σ_2_._ Moreover

E_t−_1 \[_ht_+1 _− qt_+1\] = _β_1 E_t−_1 \[_ht − qt_\] = _β_1 (_ht − qt_)_._

Hence

E_t−_1 \[_ht_+_k − qt_+_k_\] = _β_1_k_(_ht − qt_)_._

Finally,

E_t−_1 \[_ht_+_k_\] = _σ_2 + _β_2_k qt − σ_2 + _β_1_k_ (_ht − qt_)_._

1.  Note that we can substitute _<sub>qt</sub>_<sub>+1</sub> in _<sub>ht</sub>_<sub>+1</sub> to obtain

_ht_+1 = _σ_2 + _α_1_ht ε_2_t −_ 1 _−_ 2_γ_1_εt_ + _α_2_ht ε_2_t −_ 1 _−_ 2_γ_2_εt_ + _β_1 (_ht − qt_) + _β_2 _qt − σ_2_._

Hence,

Vart-1 (_ht_+1) = _α_12_h_2_t_ Var _ε_2_t −_ 1 _−_ 2_γ_1_εt_ + _α_22_h_2_t_ Var _ε_2_t −_ 1 _−_ 2_γ_2_εt_

\+ 2_α_1_α_2_h_2_t_ Cov _ε_2_t −_ 1 _−_ 2_γ_1_εt,ε_2_t −_ 1 _−_ 2_γ_2_εt_

\= _α_12_h_2_t_ (2 + 4_γ_12) + _α_22_h_2_t_ (2 + 4_γ_22)

\+ 2_α_1_α_2_h_2_t_ E h_ε_4_t − ε_2_t −_ 2_γ_1_εt_3 _− ε_2_t_ \+ 1 + 2_γ_1_εt −_ 2_γ_2_ε_3_t_ \+ 2_γ_2_εt_ \+ 4_γ_1_γ_2_εt_2 i = _α_12_h_2_t_ (2 + 4_γ_12) + _α_22_h_2_t_ (2 + 4_γ_22) + 2_α_1_α_2_h_2_t_ (2 + 4_γ_1_γ_2) = h2(_α_1 + _α_2)2 + 4(_α_1_γ_1 + _α_2_γ_2)2i_h_2_t ._

1.  The _<sub>γi</sub>_ parameters allow the model to capture the correlation between stock returns and short-run (_<sub>γ</sub>_<sub>1</sub>) and long-run (_<sub>γ</sub>_<sub>2</sub>) variance. Both are expected be positive (negative correlation), but it is reasonnable to expect short-run variance to react more strongly to asset returns than long-run variance. Hence, we expect _|γ_<sub>1</sub>_| > |γ_<sub>2</sub>_|_.
2.  In this model, _<sub>ηt</sub>_ \= _<sub>λ</sub>_. Hence, under Q

_rt_+1 = _rf_ q_ht_+1_<sup>ε∗</sup><sub>t</sub>_<sub>+1</sub>_,_

_h<sub>t</sub>__, q<sub>t</sub>__._

Letting 

_h<sub>t</sub>_

_,_

and, similarly,

_qt_+1 = _σ_2 + _α_2_ht_ 2_ht_ 

_− σ_2_. q<sub>t</sub>_

By replacing _<sub>q</sub>_ in _<sub>h</sub>_, we then get

_ht_+1 _qt − σ_2

_._

Then, letting 

 _htht._

Finally, letting 

_ht_+1 = _qt_+1 + _α_1_ht_ _, qt_+1 = _σ∗_2 + _α_2_ht_ _._

(g) The pricing algorithm goes as follows:

- Using the risk-neutral form of the model in (e), simulate a large number of trajectories of variance and returns between _<sub>t</sub>_ and _<sub>t</sub>_ \+ _<sub>T</sub>_, where _<sub>t</sub>_ is the time at which the option of maturity _<sub>T</sub>_ is valued,
- On each trajectory, sum the log-returns and obtain the value of _<sub>St</sub>_<sub>+</sub>_<sub>T</sub>_ , and thus the value of

Payoff(_S<sub>t</sub>_<sub>+</sub>_<sub>T</sub>_ ),

- Discount the payoffs with the _<sub>T</sub>_\-day ahead risk-free rate prevaling at _<sub>t</sub>_, • Average the discounted payoffs to obtain the option price.

#### Solution 7.4

1.  An application of Itˆo’s lemma yields

_S_! d_t_

_σS_ d_W<sub>t</sub>_ d_Z<sub>t</sub>_ \= d_g._

1.  Under the EMM, we have: . The drift of _<sub>S</sub>_ becomes _<sub>r</sub>_

. The drift of _<sub>σ</sub>_ becomes _<sub>−λσ</sub>_ plus a linear combination of the market prices of UA price risk and variance risk

. The diffusion coefficients of _<sub>S</sub>_ and of _<sub>σ</sub>_ and the correlation coefficient are unchanged.

#### Solution 7.5

1.  The simulation of the CEV model can be written as

_S<sub>t</sub>__tε._

1.  The control variate technique consists in applying a numerical method to evaluate a derivative product _c_<sub>b</sub> for which an analytical solution _<sub>c</sub>_ is available, and then to reduce the error of evaluation made by this same method on the derivative product _<sub>g</sub>_<sub>b</sub> by correcting the error (or a fraction of the error) made on the derivative product _<sub>c</sub>_ (called the control variable). Thus, the corrected value for the derivative product is

_g_ \= _g_<sub>b</sub> \+ _c − c._<sub>b</sub>

1.  We have an analytical solution for the European option in the SRCEV model, i.e. in the case where _α_ \= 0_<sub>.</sub>_5\. We can therefore use this analytical result as a control variate for the European option in the CEV model with any _<sub>α</sub>_.

#### Solution 7.6

1.  Mean-reversion of variance requires that 0 _<sub>< b <</sub>_ 1.
2.  Given that _<sub>a</sub> − <sub>bv</sub>_ \= _<sub>b</sub> <sup>a</sup><sub>b</sub> − <sub>v</sub>_, the equilibrium value of variance is _<sub>a/b</sub>_. (c) Parameter _<sub>c</sub>_.
3.  Parameter _<sub>d</sub>_.
4.  Unchanged parameters are _<sub>c</sub>_ and _<sub>d</sub>_.

**Chapter 8**

**Jump-diffusion models**

The introduction of jumps into the dynamics of the underlying asset allows for a more flexible modelling of market price behavior. Indeed, market participants commonly acknowledge that the arrival of new information can create abrupt changes in prices. According to the efficient market hypothesis, these phenomena can be interpreted as market ”surprises”. Unanticipated news cause drastic revisions of the supply and demand for an asset, which may induce jumps in its price process. The addition of jumps to the diffusion price dynamics brings new issues. First, just as the introduction of stochastic volatility, jumps make the market incomplete by construction. This raises the question of characterizing a risk premium for that additional source of risk. Second, the design of a model with jumps must deal with new trade-offs between realism and parsimony: How many jumps to consider? How to model jump intensity and magnitude? How to relate these intensity and magnitude with other model inputs? Third, from an econometric standpoint, the implementation of a jump-diffusion model must rely on disentangling diffusion and jumps from time-series data.

**8.1 Basics of the Poisson process**

The standard Poisson process, denoted by _<sub>{N</sub>_(_<sub>t</sub>_)_<sub>}t≥</sub>_<sub>0</sub>, is the stochastic process commonly employed for the modelling of jumps in financial time-series. It is a counting process, therefore taking values in N.

Specifically, consider a series of ”events” whose timings _<sub>{τn}n∈</sub>_<sub>N</sub> are driven by a collection of independent and identically distributed (i.i.d.) random variables following an exponential law with parameter _<sub>λ</sub>_.

P(_τn_+1 _∈_ d_t|τn_ \= _t_0) = _λe−λ_d_t._

The process _<sub>N</sub>_(_<sub>t</sub>_) counts the number of events occurring within the interval \[0_<sub>,t</sub>_\]. Figure 8.1 presents a graphic representation of a standard Poisson process

217

Figure 8.1: Standard Poisson process.

**Proposition 8.1** _The stochastic process {<sub>N</sub>_(_<sub>t</sub>_)_}<sub>t≥</sub>_<sub>0</sub> _is a standard Poisson process if and only if it satisfies the following three properties:_

1.  _The process starts at 0, i.e., <sub>N</sub>_(0) = 0_,_
2.  _The process has independent increments, i.e., for any <sub>s</sub> and <sub>t</sub> such that <sub>s < t</sub>, <sub>N</sub>_(_<sub>t</sub>_)_<sub>−N</sub>_(_<sub>s</sub>_) _is independent of N_(_s_)_,_
3.  _The increments are exponentially distributed, i.e., for any integer <sub>n</sub>_

P(_N_(_t_) _− N_(_s_) = _n_) = (_λ_(_t −_! _s_))_n_ exp(_−λ_(_t − s_))_._

_n_

Parameter _<sub>λ</sub>_ is commonly referred to as the _intensity_ of the Poisson process. Over an infinitesimal time interval

d_N_(_t_) = ( 10 with probabilitywith probability 1_λ−_d_t_,_λ_d_t_.

By construction, the Poisson process is increasing and therefore is not a martingale. Note that, for any _<sub>s</sub>_ and _<sub>t</sub>_ such that _<sub>s < t</sub>_,

E_<sub>s</sub>_  _n ×_ P(_N_(_t_) _− N_(_s_) = _n_) = _λ_(_t − s_)_._

_n_\=0

Consequently, the process _<sub>N</sub>_(_<sub>t</sub>_)_<sub>−λt</sub>_ is a martingale under the natural filtration. The term _<sub>λt</sub>_ is sometimes called the _compensator_ of the Poisson process, that is, it is the quantity that ”compensates” the Poisson process to make it a martingale.

**8.2 Some models with jumps**

#### 8.2.1 The (original) Merton model

Merton’s (1976) work laid the foundations for this family of models. The original version of the model goes as follows. The underlying asset price process _<sub>{S</sub>_(_<sub>t</sub>_)_<sub>}t≥</sub>_<sub>0</sub> combines a diffusion that accounts for regular price fluctuations and a jump component reflecting the impact of sudden news on the market. Under measure P

<sup>d</sup>(_<sup>S</sup>t_<sup>(</sup>_<sup>−t</sup>_)<sup>)</sup> \= _µ_d_t_ \+ _σ_ d_W_(_t_) + <sup>h</sup>_<sub>e</sub><sup>J</sup> −_ 1 d_N_(_t_) _− λµ<sub>J</sub>_ d_t_<sup>i</sup>_, S_

where the Brownian motion _<sub>W</sub>_(_<sub>t</sub>_) and the Poisson process _<sub>N</sub>_(_<sub>t</sub>_) are independent, and _<sub>Yn</sub>_ \= _<sub>e</sub><sup>Jn</sup> <sub>−</sub>_ 1 is the random percentage jump, conditional on jump _<sub>n</sub>_ occurring. The process _<sub>Y</sub>_  _<sub>Yn</sub>_ is referred to as a _compound_ Poisson process.

Consider independent and identically distributed and let _<sub>µJ</sub>_ \= E<sup>Ph</sup>_<sub>e</sub><sup>Jn</sup>_ _<sub>n</sub>_. For _<sub>µ</sub>_ to be interpreted as the underlying asset’s instantaneous expected return, the drift has to be compensated by

EPh_eJ −_ 1 d_N_(_t_)i = EP \[d_N_(_t_)\]EPh_eJ −_ 1i = _λµJ_ d_t._

Otherwise stated, _<sub>Y</sub>_<sub>0</sub>(_<sub>t</sub>_) = _<sub>Y</sub>_ (_<sub>t</sub>_) _− <sub>λµJ</sub> t_ is a martingale.

Merton (1976) assumes that jump risk is diversifiable and pays particular attention to the special case where _<sub>Jn</sub>_ ), with . Under these assumptions, the risk-neutral dynamics follows from applying the Girsanov theorem to the Brownian motion _<sub>W</sub>_, with price of (diffusive) risk

:

<sup>d</sup>(_<sup>S</sup>t_<sup>(</sup>_<sup>−t</sup>_)<sup>)</sup> \= _r_d_t_ \+ _σ_ d_W_<sup>Q</sup>(_t_) + d_Y_<sub>0</sub>(_t_)_,_

_S_

where the distribution of jumps is left unchanged by the passage from P to Q. The solution of this stochastic differential equation is

_S_(_t_) = _S_(0)exp_r − λµ<sub>J</sub> −_ <sup>1</sup>2_σ_<sup>2</sup> d_t_ \+ _σW_<sup>Q</sup>(_t_)exp<sup></sup>_<sup>N</sup><sub>n</sub>_<sup>X</sup><sub>\=1</sub><sup>(</sup>_<sup>t</sup>_<sup>)</sup> _J<sub>n</sub>_<sup></sup>_._ (8.1)

That is, between two jumps, the underlying behaves as it would under the Black-Merton-Scholes assumptions. Hence, it can be demonstrated that the price of a call under the Merton (1976) model is

_n_

_∞ λτ_b

_n_<sup>X</sup>\=0 _e<sup>−</sup>_<sub>b</sub>_<sup>λτ</sup>_ ! _c<sub>bms</sub>_ (_S_(_t_)_,K,r<sub>n</sub>,y,τ,σ<sub>n</sub>_) (8.2)

_n_

where _<sub>τ</sub>_ \= _<sub>T</sub> − <sub>t</sub>_ and _<sub>cbms</sub>_ is the BMS closed-form price and

_λ_<sub>b</sub> \= _λ_(1 + _µ<sub>J</sub>_)_, r<sub>n</sub>_ \= _r − λµ<sub>J</sub>_ \+ _<sup>n</sup>_ log(1 + _µ<sub>J</sub>_)_, σ<sub>n</sub>_<sup>2</sup> \= _σ_<sup>2</sup> \+ _<sup>n</sup>σ<sub>J</sub>_<sup>2</sup>_._ (8.3) _τ τ_

In short, the Merton price is a weighted average of the BMS prices, each of which is conditional on exactly _<sub>n</sub>_ jumps occurring. The weight of price _<sub>n</sub>_ is the probability of exactly _<sub>n</sub>_ jumps occurring, and the risk-neutral drift, _<sub>rn</sub>_, and variance _<sub>σn</sub>_, are adjusted to reflect the impact of the _<sub>n</sub>_ jumps.

The impact on the drift depends on the sign of the average jump _<sub>µJ</sub>_: If it is negative (resp. positive), the risk-neutral drift in absence of jumps, _<sub>r</sub>_<sub>0</sub>, is higher (lower) than the risk-free rate due to the compensator. As the number of jumps increases, their negative (positive) expected magnitude lowers (increases) the drift in the _<sub>n</sub>_<sup>th</sup> option price. Remember the _<sub>cbms</sub>_ increases with the risk-free rate; _<sub>pbms</sub>_ decreases with _<sub>r</sub>_. Regarding variance, facing _<sub>n</sub>_ jumps unambiguously increases the (annualized) variance of the underlying, raising the value of both calls and puts.

The jump-diffusion model accomodates various shapes for the smile. The smiles in Figure 8.2 are generated with a varying jump size mean: _<sub>αJ</sub>_ \= _<sub>−</sub>_0_<sub>.</sub>_2 (short-dashed line), _<sub>αJ</sub>_ \= 0 (long-dashed line), and _α<sub>J</sub>_ \= 0_<sub>.</sub>_2 (solid line). The smiles in Figure 8.2 are generated with a varying jump size volatility: _<sub>σJ</sub>_ \= 0_<sub>.</sub>_2 (short-dashed line), _<sub>σJ</sub>_ \= 0_<sub>.</sub>_4 (long-dashed line), and _<sub>σJ</sub>_ \= 0_<sub>.</sub>_6 (solid line). In both figures, the diffusion coefficient _<sub>σ</sub>_ is 0.3, represented by a dotted line for reference.

0.7

0.8

0.9

1.0

1.1

1.2

1.3

Moneyness (K/S)

25

30

35

40

45

50

55

60

Implied Volatility

_J_

\= -0.2

_J_

\= 0.0

_J_

\= 0.2

0.7

0.8

0.9

1.0

1.1

1.2

1.3

Moneyness (K/S)

30

40

50

60

70

Implied Volatility

_J_

\= 0.1

_J_

\= 0.2

_J_

\= 0.4

Figure 8.2: Varying the jump size mean. Figure 8.3: Varying the jump size volatility.

The impact of jump intensity on the smile is shown in Figure 8.4 with _<sub>λ</sub>_ \= 0_<sub>.</sub>_2 (short-dashed line), _<sub>λ</sub>_ \= 0_<sub>.</sub>_4 (long-dashed line), and _<sub>λ</sub>_ \= 0_<sub>.</sub>_6

0.7

0.8

0.9

1.0

1.1

1.2

1.3

Moneyness (K/S)

30

40

50

60

Implied Volatility

\= 1/2

\= 1

\= 2

(solid line).

Whereas the sign of _<sub>αJ</sub>_ controls the (sign of) skewness and the magnitude of _<sub>σJ</sub>_ the excess kurtosis, the intensity of jumps _<sub>λ</sub>_ shifts the level of the IV curve.

Figure 8.4: Varying the jump intensity.

#### 8.2.2 Priced jump risk

Assuming that jump risk is diversifiable might not be innocuous, and could be outright contradictory if the underlying asset is already a broadly diversified index. We will thus consider a generalization of the Girsanov theorem that will allow for a richer risk-neutralization of the Merton model. Consider the following Radon-Nikodym derivative (see, e.g., Cont and Tankov, 2004, Cheang and Chiarella, 2012)

 dQ = _ξ_(_t_) = exp_−ηwWN_X(_t_) (_ηλ_ \+ _ηJJn_) _− λµ′Jt__,_ (8.4)

dP_t_ _n_\=1 

with _<sub>µ</sub><sup>′</sup><sub>J</sub>_ \= _<sub>e</sub><sup>ηλ</sup>_ E<sup>Ph</sup>_<sub>e</sub><sup>ηJJ</sup>_<sup>i</sup> _<sub>−</sub>_ 1\. It can be shown that _<sub>ξ</sub>_(_<sub>t</sub>_) is a martingale under P with expectation equal to

1.

Thus, a family of EMM Q can be obtained using different _<sub>ηw</sub>_ (adjusting for Brownian risk) and _<sub>ηλ</sub>_ and _η<sub>J</sub>_ (adjusting for jump intensity and magnitude risk).

**Proposition 8.2** _(Girsanov) Under the change of probability measure (8.4),_

_(i) The process <sub>W</sub>_<sup>Q</sup>(_<sub>t</sub>_) = _<sub>W</sub>_(_<sub>t</sub>_) + _<sub>ηwt</sub> is a Brownian motion under_ Q_, (ii) The process_ <sup>P</sup>_<sup>N</sup><sub>n</sub>_<sub>\=1</sub><sup>(</sup>_<sup>t</sup>_<sup>)</sup> _<sub>Jn</sub> is a compound Poisson process with new intensity_

_λ_e = _λ_ 1 + _µ′J_

_and a new jump size distribution with moment generating function_

h i EPh_e_(_ηJ_+_u_)_J_i

EQ _euJ_ \= EP \[_eηJJ_\] _._

If the jump size distribution under P belongs to the exponential family, then the jump size distribution under Q remains the same, but with modified parameters. If _<sub>ηλ</sub>_ \= 0 and _<sub>ηJ</sub>_ \= 0_<sub≯</sub>_ , the EMM dynamics imply a change in jump size distribution, hence a change in intensity as well. If _<sub>ηJ</sub>_ \= 0 and _<sub>ηλ</sub>_ \= 0_<sub≯</sub>_ , the EMM dynamics imply a change in intensity only. Although Merton (1976) pays particular attention to the special case where _<sub>ηJ</sub>_ \= _<sub>ηλ</sub>_ \= 0, it is common to refer to the jump diffusion model as the “Merton” model even under a generalized risk-neutralization.

The no-arbitrage restriction entails that

E<sup>Q</sup> \[d_S_(_t_)\] = (_r − y_)_S_(_t<sup>−</sup>_)d_t,_

where _<sub>r</sub>_ is the risk-free rate and _<sub>y</sub>_ is the continuous dividend yield. It follows that the Q-dynamics for the underlying asset are given by

d_S_(_t_) = _r − y − λ_e_µ_e_J_ d_t_  d_N_Q(_t_)_,_ (8.5)

_S_(_t−_)

where the compound Poisson process <sup>P</sup>_<sup>N</sup><sub>n</sub>_<sub>\=1</sub><sup>(</sup>_<sup>t</sup>_<sup>)</sup> _<sub>Jn</sub>_ has intensity _<sub>λ</sub>_<sub>e</sub> and expected jump size _<sub>µ</sub>_<sub>e</sub>_J_ \= EQ<sup>h</sup>_<sub>e</sub><sup>Jn</sup>_ .

The change in drift reflects the risk premium correction

_µ −_ (_r − y_) = _ση<sub>w</sub>_ \+ _λµ<sub>J</sub> − λ_<sub>e</sub>_µ_e_J,_

where _<sub>σηw</sub>_ is the premium for diffusion risk and _<sub>λµJ</sub> − <sub>λ</sub>_<sub>e</sub>_<sub>µ</sub>_<sub>e</sub>_J_ is the premium for jump risk. The solution to equation (8.5) can be written as

<sup></sup>_N_(_t_) <sup></sup>

_S_(_t_) = _S_(0)exp_r_X _J<sub>n</sub>__._ (8.6)

_n_\=1 

which is analog to equation (8.1), but once again reflecting the premium for jump risk.

Generalizing Merton (1976), jump sizes _<sub>Jn</sub>_ under Q are now distributed _<sub>Jn</sub>_), with

1 2

_α_e_J_ \= _αJ_ \+ _ηJσJ_<sup>2</sup> \= log(1 + _µJ_) + _ηJ −_ 2 _σJ ⇒_ 1 + _µ_e_J_ \= 1 + _µJeηJσJ_2 _,_

and jump intensity under Q is given by

_λ_e = _λ_ 1 + _µ′J__._

|     |     |
| --- | --- |
| Equation (8.2) still holds<br><br>_n_<br><br>_∞ λτ_b<br><br>_<sub>n</sub>_<sup>X</sup><sub>\=0</sub> _<sup>−</sup>_<sup>b</sup>_<sup>λτ</sup>_ ! _cbms_ (_S_(_t_)_,K,r<sub>n</sub>,y,τ,σ<sub>n</sub>_) _e_<br><br>_n_<br><br>but we now have |     |
| _λ_<sub>b</sub> \= _λ_<sub>e</sub> (1 + _µ_<sub>e</sub>_J_)_, r<sub>n</sub>_ \= _r − λ_<sub>e</sub>_µ_<sub>e</sub>_J_ \+ _<sup>n</sup><sub>τ</sub>_ log(1 + _µ_<sub>e</sub>_J_)_, σ<sub>n</sub>_<sup>2</sup> \= _σ_<sup>2</sup> \+ _<sup>n</sup><sub>τ</sub> σ<sub>J</sub>_<sup>2</sup>_._ | (8.7) |

Hence, these price of risk parameters are not material if one only cares about the risk-neutral measure. However, if the parameters of the Merton model are meant to describe the physical dynamics of the underlying, the prices of jump intensity risk _<sub>ηλ</sub>_, and jump size risk _<sub>ηJ</sub>_ allow for a larger increase in the IV, skewness and kurtosis under Q, as illustrated in Figures 8.5 and 8.6.

0.7

0.8

0.9

1.0

1.1

1.2

1.3

Moneyness (K/S)

25

30

35

40

45

50

55

60

Implied Volatility

\= 0.0

\= 0.2

\= 0.4

Figure 8.5: Varying the jump intensity premium.

0.7

0.8

0.9

1.0

1.1

1.2

1.3

Moneyness (K/S)

25

30

35

40

45

50

55

60

Implied Volatility

_J_

\= -0.5

_J_

\= 0.0

_J_

\= 0.5

Figure 8.6: Varying the jump size premium.

#### 8.2.3 Discrete-time algorithm for American options

Amin (1993) develops an adjustment of the binomial model to incorporate multivariate jumps. Setting

_σ_2

_a_ \= _r − y − λ_<sub>e</sub>_µ_e_J −_ 2 _,_

the goal is to build a state-space representing the discrete-time dynamics for the continuous-time process

<sup></sup>_N_(_t_) <sup></sup>

_S_(_t_) = _S_(0)exp(_at_)exp_σW_<sub></sub><sup>X</sup> _J<sub>n</sub>_<sub></sub>_._

_n_\=1

Amin (1993) considers an extension of the Jarrow-Rudd binomial tree. The trading interval \[0_<sub>,T</sub>_\] is partitioned into _<sub>Nt</sub>_ periods of length _<sub>δt</sub>_ \= _<sub>T/Nt</sub>_. Let _<sub>n</sub>_ and _<sub>j</sub>_ denote the index for time and space. The state-space for log-returns _<sub>Xn</sub>_ := ln(_<sub>S</sub>_(_<sub>nδt</sub>_)_<sub>/S</sub>_(0)) is

0

_..._

_N_

_nδt_

_δt_

_..._

_t_

_δt_

_..._

_..._

_..._

_aδt_

+

_jσ_

_√_

_δt_

_..._

_anδt_

+

_jσ_

_√_

_δt_

_..._

_aN_

_t_

_δt_

+

_jσ_

_√_

_δt_

_..._

_..._

_..._

_aδt_

+

_σ_

_√_

_δt_

_anδt_

+

_σ_

_√_

_aN_

_δt_

_t_

_δt_

+

_σ_

_√_

_δt_

0

_aN_

_aδt_

_anδt_

_t_

_δt_

_aδt_

_−_

_σ_

_√_

_anδt_

_δt_

_−_

_σ_

_√_

_aN_

_δt_

_t_

_δt_

_−_

_σ_

_√_

_δt_

_..._

_..._

_..._

_aδt_

_−_

_jσ_

_√_

_δt_

_..._

_anδt_

_−_

_jσ_

_√_

_aN_

_δt_

_..._

_t_

_δt_

_−_

_jσ_

_√_

_δt_

_..._

_..._

_..._

At each node of the state-space, the no-arbitrage value of the derivative is obtained recursively as its expected value at the next period discounted at the risk-free rate. As in any other standard tree, the no-arbitrage value of an American-style derivative is obtained as the maximum at each node between its continuation value and its exercise value. For the algorithm to be complete, one needs to specify the transition probabilities as well as the truncation rules.

For computational convenience, Amin (1993) suggests to use the adjacent nodes (states _<sub>j</sub>_+1 and _<sub>j−</sub>_1) for modelling the diffusion part exclusively. Hence

_√_

 Prob _X<sub>n</sub>_<sub>+1</sub> _− X<sub>n</sub>_ \= _aδt_ \+ _σ δt_

\= Prob_X<sub>n</sub>λδt_<sub>e</sub> _,_

which is the Jarrow-Rudd risk-neutral probability of one half conditional on no jump within _<sub>δt</sub>_ units of time. For all other states, the transition probabilities reflect the modelling of the jump component

Prob_X<sub>n</sub>_<sub>+1</sub> _̸ λδt_<sub>e</sub> d_F_ (_j_)_,_

where _<sub>F</sub>_ (_<sub>.</sub>_) stands for the risk-neutral cumulative density function of the jump magnitude.

For a proper discretization, each node is assigned a mass of probability calculated on an interval centered around the node, which yields

+

_j_

_−_

1

2

_σ_

_√_

d_F_ (_j_) = _F aδtδt_ _− F aδt δt._

One exception is for _<sub>j</sub>_ \= _<sub>±</sub>_1 since these one-notch changes of state (i.e., ”local changes”) account for the diffusion dynamics. Consequently, the probability mass corresponding to the nodes _<sub>j ∈ {−</sub>_1;0;+1_<sub>}</sub>_ is

assigned entirely to _<sub>j</sub>_ \= 0, that is, d_<sub>F</sub>_ (_<sub>±</sub>_1) = 0 and

d_F_ (0) = _F aδtδt_ _− F aδt − ._

When _<sub>F</sub>_ (_<sub>.</sub>_) is the normal cdf, the model is a discretized version of Merton (1976). In this case, Amin (1993) suggests the following truncation

_√ √_ <sub>i</sub>

<sup>h</sup>_aδt_ \+ _uσ δt_;_aδt − uσ δt ,_

where _<sub>u</sub>_ is the smallest nonnegative integer such that the region includes \[_<sub>−</sub>_3_<sub>σJ</sub>_;+3_<sub>σJ</sub>_\]. The probability mass outside the truncation region is reassigned to the truncation nodes.

#### 8.2.4 The Kou model

To get more flexibility in the modelling of jump dynamics, Kou (2002) proposes a double exponential jumpdiffusion model. Jump size distribution belongs to the exponential family: It remains the same under P and Q (with modified parameters). There are two main advantages with respect to the Merton (1976) framework: (i) the model provides more flexibility to allow for asymmetric and leptokurtic underlying asset returns, and (ii) analytical results are available for option pricing problems that involve a first hitting time (barrier options, perpetual American options...).

The underlying asset dynamics under Q is

( ! ) <sup></sup>_N_(_t_) <sup></sup>

_S_(_t_) = _S_(0)exp _r − y − λ_<sub>e</sub>_µ_<sub>e</sub>_J −_  _t_ \+ _σW_<sup>Q</sup>(_t_) exp<sup>X</sup> _J<sub>n</sub>_<sup></sup>_,_

_n_\=1  with _<sub>N</sub>_(_<sub>t</sub>_) a Poisson process with intensity _<sub>λ</sub>_<sub>e</sub> and independent jump sizes _<sub>Jn</sub>_ following an asymmetric double exponential distribution with density

_g_ (_j_) = _pζ_1_e−ζ_1_j_1_j≥_0 + (1 _− p_)_ζ_2_eζ_2_j_1_j<_0_,_

with _<sub>ζ</sub>_<sub>1</sub> _<sub>\></sub>_ 0, _<sub>ζ</sub>_<sub>2</sub> _<sub>\></sub>_ 0, and _<sub>p</sub>_ (resp. 1 _<sub>− p</sub>_) stands for the probability of an upward (resp. downward) jump.

Put differently

\= ( +_j_\+ with probability _p_,

_Jn −j−_ with probability 1 _− p_,

where _<sub>j</sub>_<sup>\+</sup> and _<sub>j</sub><sup>−</sup>_ are exponential random variables with means 1_<sub>/ζ</sub>_<sub>1</sub> and 1_<sub>/ζ</sub>_<sub>2</sub>. Note that

E_<sup>p</sup>,_ _._

#### 8.2.5 Jump diffusion with stochastic volatility

Bates (1996, 2000) augment the Merton jump diffusion model with a stochastic volatility. The underlying asset dynamics under Q is given by

d_S_((_t_)_t_) = _r − y − λ_e_µ_e_J_ d_t_ \+ q_v_(_t_)d_W_Q(_t_) + _eJ −_ 1 d_N_(_t_)_, S_

d_v_ d_t_ \+ _σ<sub>v</sub>_<sup>q</sup>_v_(_t_)d_W<sub>v</sub>_<sup>Q</sup>(_t_)_,_

where d_<sub>W</sub>_<sup>Q</sup>d_<sub>t</sub>_ and volatility risk premium is assumed to be proportional to variance, as in

Heston (1993).

This approach yields analytical formulae for European options. They exhibit the same functional form as in Heston (1993)

_c_ \= _e<sup>−rT</sup>_ (_F × P_<sub>1</sub> _− K × P_<sub>2</sub>)_,_

except that the moment generating function

_Fj_ (_x,v,T_) = EQj _ex_ln _S_(0) _, j_ \= 1_,_2

includes a correction for the presence of jumps.

**8.3 Simulating jump-diffusion models**

A simple way to simulate a jump-diffusion process is to construct the path point by point with a fixed time interval _<sub>δt</sub>_. Using a Euler scheme, the jump-diffusion dynamics can be discretized as follows

" ! _√_ \# <sup></sup> _N_(_t_+_δt_) <sup></sup>

_S_(_t_ \+ _δt_) = _S_(_t_)exp _r_ _µ_<sub>e</sub>_J δt_ \+ _σ δtε_ exp<sub></sub> <sup>X</sup> _J<sub>n</sub>_<sub></sub>_,_

_n_\=_N_(_t_)+1

where _<sub>ε</sub>_ is the random draw from a standard normal variable.

The process _<sub>S</sub>_ is simulated like a diffusion with the additional test that consists in determining the number of jumps occurring within _<sub>δt</sub>_. To this end, we note that the probability that no jump occurs within _<sub>δt</sub>_ is given by exp_<sub>−λδt</sub>_<sub>e</sub> . Hence the following procedure. Let _<sub>u</sub>_<sub>1</sub> denote the random draw from the uniform law over \[0_<sub>,</sub>_1\]. If _<sub>u</sub>__<sub>λδt</sub>_<sub>e</sub> , then the number of jumps is nil. Otherwise, we draw another _u_<sub>2</sub> from the uniform law over \[0_<sub>,</sub>_1\]. We repeat until we find _<sub>m</sub>_ such that

_λδt_<sub>e</sub> and Π _t,_

which implies that there are _<sub>m</sub>_ jumps within the interval _<sub>δt</sub>_.

Once the number of jumps within _<sub>δt</sub>_ is known, the simulation alogorithm goes as follows:

- Draw _<sub>m</sub>_ realizations of jump sizes from the postulated jump size distribution (e.g., normal) to determine _J_<sub>1</sub>_,...,J<sub>m</sub>_,
- Apply the correction exp(<sup>P</sup>_<sup>m</sup><sub>n</sub>_<sub>\=1</sub> _J<sub>n</sub>_) to the diffusion part,
- Proceed to next time step _<sub>δt</sub>_.

**Bibliography**

Amin K. (1993). Jump Diffusion Option Valuation in Discrete Time. _Journal of Finance_, _58_, 1833–1863.

Amin K., & Ng V. (1993). _ARCH Processes and Option Valuation_. working paper, University of Michigan.

Anderluh J., & van der Weide H. (2004). Parisian Options – The Implied Barrier Concept. In M. Bubak, G. D. van Albada, P. M. A. Sloot, & J. Dongarra (Eds.), _Computational science - iccs 2004_ (pp. 851– 858). Springer Berlin Heidelberg.

Angus J. (1999). A Note on Pricing Asian Derivatives with Continuous Geometric Averaging. _Journal of Futures Markets_, _19_, 845–858.

Babbs S. (2000). Binomial Valuation of Lookback Options. _Journal of Economic Dynamics and Control_, _24_, 1499–1525.

Barone-Adesi G., & Whaley R. (1986). The Valuation of American Call Options and the Expected ExDividend Stock Price Decline. _Journal of Financial Economics_, _17_, 91–111.

Barone-Adesi G., & Whaley R. (1987). Efficient Analytic Approximation of American Option Values. _Journal of Finance_, _42_, 301–320.

Barraquand J., & Martineau D. (1995). Numerical Valuation of High Dimensional Multivariate American Securities. _Journal of Financial and Quantitative Analysis_, _30_, 383–405.

Basu S., & Hull J. (2021). _Options, Futures and Other Derivatives_. Pearson.

Bates D. (1996). Jumps and Stochastic Volatility: Exchange Rate Processes Implicit in Deustche Mark Options. _Review of Financial Studies_, _9_, 69–107.

Bates D. (2000). Post-’87 Crash Fears in the S&P 500 Futures Option Market. _Journal of Econometrics_, _94_(1/2), 181–238.

Beckers S. (1980). The Constant Elasticity of Variance Model and its Implications for Option Pricing. _Journal of Finance_, _35_, 661–673.

Bergman Y., Grundy B., & Wiener Z. (1996). General Properties of Option Prices. _Journal of Finance_, _51_, 1573–1610.

Bernard C., & Boyle P. (2011). Monte Carlo Methods for Pricing Discrete Parisian Options. _European Journal of Finance_, _17_, 169–196.

Bjerksund P., & Stensland S. (2014). Closed Form Spread Option Valuation. _Quantitative Finance_, _14_, 1785–1794.

Black F. (1976). The Pricing of Commodity Contracts. _Journal of Financial Economics_, _3_, 167–179.

Black F., & Scholes M. (1973). The Pricing of Options and Corporate Liabilities. _Journal of Political Economy_, _81_, 637–654.

227

Bollerslev T. (1986). Generalized Autoregressive Conditional Heteroscedasticity. _Journal of Econometrics_, _31_, 307–327.

Bollerslev T., Chou R., & Kroner K. (1992). Arch Modelling in Finance: A Review of the Theory and Empirical Evidence. _Journal of Econometrics_, _51_, 5–59.

Bossaerts P., & Hillion P. (1997). Local Parametric Analysis of Hedging in Discrete Time. _Journal of Econometrics_, _81_, 243–272.

Boyle P. (1977). Options: A Monte Carlo Approach. _Journal of Financial Economics_, _4_, 323–338.

Boyle P. (1986). Option Valuation Using a Three-jump Process. _International Options Journal_, _3_, 7–12.

Boyle P. (1988). A Lattice Framework for Option Pricing with Two State Variables. _Journal of Financial and Quantitative Analysis_, _23_, 1–12.

Boyle P., & Emanuel D. (1980). Discretely Adjusted Option Hedges. _Journal of Financial Economics_, _8_, 259–282.

Boyle P., & Vorst T. (1992). Option Replication in Discrete Time with Transaction Costs. _Journal of Finance_, _47_, 271–293.

Breeden M., & Litzenberger R. (1978). Prices of State Contingent Claims Implicit in Option Prices. _Journal of Business_, _51_, 621–651.

Brennan M., & Schwartz E. (1978). Finite Difference Methods and Jump Processes Arising in the Pricing of Contingent Claims: A Synthesis. _Journal of Financial and Quantitative Analysis_, _13_, 462–474.

Broadie M., & Detemple J. (1996). American Option Valuation: New Bounds, Approximations, and a Comparison of Existing Methods. _Review of Financial Studies_, _9_, 1211–1250.

Broadie M., & Glasserman P. (1997). Pricing American-Style Securities Using Simulation. _Journal of Economic Dynamics and Control_, _21_, 1323–1352.

Broadie M., & Glasserman P. (1998). Simulation for Option Pricing and Risk Management. _Risk Management and Analysis_, _1_, 173–207.

Broadie M., Glasserman P., & Kou S. (1997). A Continuity Correction for Discrete Barrier Options. _Mathematical Finance_, _7_, 325–348.

Broadie M., & Kaya O. (2006). Exact Simulation of Stochastic Volatility and Other Affine Jump Diffusion¨ Processes. _Operations Research_, _54_, 217–231.

Carmona R., & Durrleman V. (2003). Pricing and Hedging Spread Options. _SIAM Review_, _45_, 627–685.

Carr P., Jarrow R., & Myneni R. (1992). Alternative Characterizations of American Puts. _Mathematical Finance_, _2_, 87–106.

Carri\`ere J. (1996). Valuation of Early-Exercise Price of Options Using Simulations and Nonparametric Regression. _Insurance: Mathematics and Economics_, _19_, 19–30.

Cheang G., & Chiarella C. (2012). _A Modern View on Merton’s Jump-Diffusion Model_. Stochastic Processes, Finance; Control: A Festschrift in Honor of Robert J Elliott.

Chesney M., & Gibson R. (1995). State Space Symmetry and Two-Factor Option Pricing Models. _Advances in Futures and Options Research_, _8_, 85–112.

Chesney M., Jeanblanc M., & Yor M. (1997). Brownian Excursions and Parisian Barrier Options. _Advances in Applied Probabilities_, _29_, 165–184.

Chesney M., & Lefoll J. (1996). Predicting Premature Exercise of an American Put on Stocks: Theory and Empirical Evidence. _European Journal of Finance_, _2_, 21–39.

Cheuk T., & Vorst T. (1997). Currency Lookback Options and Observation Frequency: A Binomial Approach. _Journal of International Money and Finance_, _16_, 173–187.

Christoffersen P., Dorion C., Jacobs K., & Wang Y. (2010). Volatility Components, Affine Restrictions and Non-Normal Innovations. _Journal of Business and Economic Statistics_, _28_, 483–502.

Christoffersen P., & Jacobs K. (2004). Which GARCH Option Model for Valuation? _Management Science_, _50_, 1204–1221.

Cl´ement E., Lamberton D., & Protter P. (2002). An Analysis of a Least Squares Regression Algorithm for American Option Pricing. _Finance and Stochastics_, _6_, 449–471.

Clewlow L., & Carverhill A. (1994). On the Simulation of Contingent Claims. _Journal of Derivatives_, _2_, 66–74.

Cont R., & Tankov P. (2004). _Financial Modelling with Jump Processes_. Chapman; Hall/CRC.

Conze A., & Viswanathan M. (1991a). European Path Dependent Options: The Case of Geometric Averages. _Finance_, _12_(1), 7–22.

Conze A., & Viswanathan M. (1991b). Path Dependent Options: The Case of Lookback Options. _Journal of Finance_, _46_, 1893–1907.

Cox J. (1996). The Constant Elasticity of Variance Option Pricing Model. _Journal of Portfolio Management_, 15–17.

Cox J., Ingersoll J., & Ross S. (1981). The Relation Between Forward Prices and Futures Prices. _Journal of Financial Economics_, _9_, 321–346.

Cox J., & Ross S. (1976). The Valuation of Options for Alternative Stochastic Processes. _Journal of Financial Economics_, _3_, 145–166.

Cox J., Ross S., & Rubinstein M. (1979). Option Pricing: A Simplified Approach. _Journal of Financial Economics_, _7_, 229–263.

Davis M., Panas V., & Zariphopoulou T. (1993). European Option Pricing with Transaction Costs. _SIAM Journal of Control and Optimization_, _31_, 470–493.

Dewynne J., & Wilmott P. (1995). Asian Options as Linear Complementarity Problems: Analysis and Finite-Difference Solutions. _Advances in Futures and Options Research_, _8_, 145–177.

Ding Z., Granger C., & Engle R. (1993). A Long Memory Property of Stock Market Returns and a New Model. _Journal of Empirical Finance_, _1_, 83–106.

Dragulescu A., & Yakovenko V. (2002). Probability Distribution of Returns in the Heston Model with Stochastic Volatility. _Quantitative Finance_, _2_, 443–453.

Duan J. (1995). The Garch Option Pricing Model. _Mathematical Finance_, _5_, 13–32.

Duan J., Gauthier G., Sasseville C., & Simonato J.-G. (2004). _Approximating the GJR-GARCH and EGARCH Option Pricing Models Analytically_. working paper, HEC Montr´eal.

Duan J., & Simonato J.-G. (1998). Empirical Martingale Simulation for Asset Prices. _Management Science_, _44_, 1218–1233.

Engle R., & Ng V. (1993). Measuring and Testing the Impact of News on Volatility. _Journal of Finance_, _48_, 1749–1778.

Fama E. (1965). The Behavior of Stock Market Prices. _Journal of Business_, _38_, 34–105.

Fama E. (1970). Efficient Capital Markets: A Review of Theory and Empirical Work. _Journal of Finance_, _25_, 383–417.

Figlewski S., & Gao B. (1999). The Adaptive Mesh Model: A New Approach to Efficient Option Pricing. _Journal of Financial Economics_, _53_, 313–351.

French K. (1980). Stock Returns and the Weekend Effect. _Journal of Financial Economics_, _8_, 55–69.

Fusai G., & Tagliani A. (2001). Pricing of Occupation Time Derivatives: Continuous and Discrete Monitoring. _Journal of Computational Finance_, _5_, 1–37.

Geske R. (1977). The Valuation of Corporate Liabilities as Compound Options. _Journal of Financial and Quantitative Analysis_, _12_, 541–552.

Geske R. (1979). The Valuation of Compound Options. _Journal of Financial Economics_, _7_, 63–81.

Gesser V., & Poncet P. (1997). Volatility Patterns: Theory and Evidence from the Dollar-Mark Option Market. _Journal of Derivatives_, _5_, 46–61.

Glasserman P. (2004). _Monte Carlo Methods in Financial Engineering_. Springer.

Glosten L., Jagannathan R., & Runkle D. (1993). On the Relationship between the Expected Value and the Volatility of the Nominal Excess Return on Stocks. _Journal of Finance_, _48_, 1779–1801.

Goldman B., Sosin H., & Gatto M. (1979). Path Dependent Options: Buy at the Low, Sell at the High. _Journal of Finance_, _34_, 1111–1127.

Haber R., Sch¨onbucher P., & Wilmott P. (1999). Pricing Parisian Options. _Journal of Derivatives_, _6_, 71–79.

Hagan P., Kumar D., Lesniewski A., & Woodward D. (2002). Managing smile risk. _Wilmott Magazine_, _1_, 84–108.

Harrison M., & Kreps D. (1979). Martingales and Arbitrage in Multiperiod Securities Markets. _Journal of Economic Theory_, _20_, 381–408.

Harrison M., & Pliska S. (1981). Martingales and Stochastic Integrals in the Theory of Continuous Trading. _Stochastic Processes and their Applications_, _11_, 215–260.

Hauser S., & Lauterbach B. (1996). Tests of Warrant Pricing Models: The Trading Profits Perspective. _Journal of Derivatives_, _4_(2), 71–79.

Henrotte P. (1993). _Transaction Costs and Duplication Strategies_. Working Paper, HEC Paris.

Hentschel L. (1995). All in the Family: Nesting Symmetric and Asymmetric GARCH Models. _Journal of Financial Economics_, _39_, 71–104.

Heston S. (1993). A Closed Form Solution for Options with Stochastic Volatility with Applications to Bonds and Currency Options. _Review of Financial Studies_, _6_, 327–343.

Heston S. (1997). _A Simple New Formula for Options with Stochastic Volatility_. Working Paper, Washington University.

Heston S., & Nandi S. (2000). A Closed-form GARCH Option Pricing Model. _Review of Financial Studies_, _13_, 585–626.

Hodges S., & Neuberger A. (1989). Optimal Replication of Contingent Claims under Transaction Costs. _Review of Futures Markets_, _8_, 222–239.

Hoggard T., Whalley E., & Wilmott P. (1994). Hedging Option Portfolios in the Presence of Transaction Costs. _Advances in Futures and Options Research_, _7_, 21–35.

Hsieh K., & Ritchken P. (2005). An Empirical Comparison of GARCH Option Pricing Models. _Review of Derivatives Research_, _8_, 129–150. https://doi.org/10.1007/s11147-006-9001-3

Huang J., Subrahmanyam M., & Yu G. (1996). Pricing and Hedging American Options: A Recursive Integration Method. _Review of Financial Studies_, _9_, 277–300.

Hugonnier J. (1999). The Feynman-Kac Formula and Pricing Occupation-Time Derivatives. _International Journal of Theoretical and Applied Finance_, _2_, 153–178.

Hui C. H., Lo C., & Yuen P. (2000). Constant Elasticity of Variance Option Pricing Model with TimeDependent Parameters. _International Journal of Theoretical and Applied Finance_, _3_, 661–674.

Hull J., & White A. (1987). The Pricing of Options on Assets with Stochastic Volatilities. _Journal of Finance_, _42_, 281–300.

Hull J., & White A. (1988). The Use of the Control Variate Technique in Option Pricing. _Journal of Financial and Quantitative Analysis_, _23_(3), 237–251.

Hull J., & White A. (1990a). Pricing Interest Rate Derivative Securities. _Review of Financial Studies_, _3_(4), 573–592.

Hull J., & White A. (1990b). Valuing Derivative Securities Using the Finite Difference Method. _Journal of Financial and Quantitative Analysis_, _25_(1), 87–100.

Ib´an˜ez A., & Zapatero F. (2004). Monte Carlo Valuation of American Options through Computation of the Optimal Exercise Frontier. _Journal of Financial and Quantitative Analysis_, _39_, 253–275. https://doi.org/10.1017/S0022109000003069

Itˆo K. (1944). Stochastic integral. _Proceedings of the Imperial Academy_, _20_(8), 519–524. [https://doi.org/](https://doi.org/10.3792/pia/1195572786)

[10.3792/pia/1195572786](https://doi.org/10.3792/pia/1195572786)

Jacka S. (1991). Optimal Stopping and the American Put. _Mathematical Finance_, _1_, 1–14.

Jagannathan R. (1984). Call Options and the Risk of Underlying Securities. _Journal of Financial Economics_, _13_, 425–434.

Jamshidian F. (1992). An Analysis of American Options. _Review of Futures Markets_, _11_, 72–82.

Jarrow R., & Oldfield G. (1981). Forward Contracts and Futures Contracts. _Journal of Financial Economics_, _9_, 373–382.

Jarrow R., & Rudd A. (1983). _Option Pricing_. R. Irwin, Homewood.

Ju N. (1998). Pricing an American Option by Approximating Its Early Exercise Boundary as a Multipiece Exponential Function. _Review of Financial Studies_, _11_, 627–646.

Kahl C., & J¨ackel P. (2006). Fast Strong Approximation Monte Carlo Schemes for Stochastic Volatility Models. _Quantitative Finance_, _6_, 513–536.

Karatzas I., & Shreve S. E. (1991). _Brownian Motion and Stochastic Calculus_ (Second). Springer-Verlag.

Kemna A., & Vorst A. (1990). A Pricing Method for Options Based on Average Asset Values. _Journal of Banking and Finance_, _14_, 113–129.

Kim I. (1990). The Analytical Valuation of American Options. _Review of Financial Studies_, _3_, 547–572.

Kirk E. (1995). Correlation in the Energy Markets. In _Managing energy price risk_ (pp. 71–78). Risk Publications; Enron.

Kou S. (2002). A Jump-Diffusion Model for Option Pricing. _Management Science_, _48_, 1086–1101.

Leisen D., & Reimer M. (1996). Binomial Models for Option Valuation: Examining and Improving Convergence. _Applied Mathematical Finance_, _3_, 319–346.

Leland H. (1985). Option Pricing and Replication with Transaction Costs. _Journal of Finance_, _40_, 1283– 1301.

Longstaff F., & Schwartz E. (2001). Valuing American Options by Simulation: A Simple Least-Squares Approach. _Review of Financial Studies_, _14_, 113–147.

Lord R., Koekkoek R., & Dijk D. (2010). A Comparison of Biased Simulation Schemes for Stochastic Volatility Models. _Quantitative Finance_, _10_, 177–194.

MacMillan L. (1986). Analytic Approximation for the American Put Option. _Advances in Futures and Options Research_, _1_, 119–139.

Margrabe W. (1978). The Value of an Option to Exchange One Asset for the Other. _Journal of Finance_, _33_, 177–186.

Martellini L. (2000). Efficient Option Replication in the Presence of Transaction Costs. _Review of Derivatives Research_, _4_, 107–131.

Martellini L., & Priaulet P. (2002). Competing Methods for Option Hedging in the Presence of Transaction Costs. _Journal of Derivatives_, _9_, 26–38.

McDonald R., & Schr¨oder M. (1998). A Parity Result for American Options. _Journal of Computational Finance_, _1_, 5–13.

Melino A., & Turnbull S. (1995). Misspecification and the Pricing and Hedging of Long Term Foreign Currency Options. _Journal of International Money and Finance_, _14_, 373–393.

Merton R. (1976). Option Pricing with Discontinuous Returns. _Journal of Financial Economics_, _3_, 125– 144.

Merton R. (1973). Theory of Rational Option Pricing. _Bell Journal of Economics and Management Science_, _4_, 141–183.

Mohamed B. (1994). Simulation of Transaction Costs and Optimal Rehedging. _Applied Mathematical Finance_, _1_, 49–62.

Moraux F. (2019). On Bankruptcy Procedures and the Valuation of Corporate Securities. _Finance_, _40_(3), 141–191.

Nandi S. (1998). How Important is the Correlation between Returns and Volatility in a Stochastic Volatility Model? Empirical Evidence from Pricing and Hedging in the S&P 500 Index Options Market. _Journal of Banking and Finance_, _22_, 589–610.

Nelson D. (1990). ARCH Models as Diffusion Approximations. _Journal of Econometrics_, _45_, 7–38.

Nelson D. (1991). Conditional Heteroskedasticity in Asset Returns: A New Approach. _Econometrica_, _59_, 347–370.

Omberg E. (1987). The Valuation of American Puts with Exponential Exercise Policies. _Advances in Futures and Options Research_, _2_, 117–142.

Palmer K. (2001). A Note on the Boyle-Vorst Discrete-Time Option Pricing Model with Transactions Costs. _Mathematical Finance_, _11_, 357–363.

Platen E., & Schweizer M. (1998). On Feedback Effects from Hedging Derivatives. _Mathematical Finance_, _8_, 67–84.

Reiner E., & Rubinstein M. (1991). Breaking Down the Barriers. _Risk_, _4_, 31–35.

Rendleman R., & Bartter B. (1979). Two-State Option Pricing. _Journal of Finance_, _34_, 1093–1110.

Ritchken P., Sankarasubramanian L., & Vijh A. (1993). The Valuation of Path Dependent Contracts on the Average. _Management Science_, _39_, 1202–1213.

Ritchken P., & Trevor R. (1999). Pricing Options Under Generalized GARCH and Stochastic Volatility Processes. _Journal of Finance_, _54_, 377–402.

Rubinstein M. (1985). Nonparametric Tests of Alternative Option Pricing Models Using All Reported Trades and Quotes on the 30 Most Active CBOE Option Classes from August 23, 1976 through August 31, 1978. _Journal of Finance_, _40_, 455–480.

Rubinstein M. (1994). Implied Binomial Trees. _Journal of Finance_, _49_, 771–818.

Rubinstein M. (1998). Edgeworth Binomial Trees. _Journal of Derivatives_, _5_, 20–27.

Schmalensee R., & Trippi R. (1978). Common Stock Volatility Expectations Implied by Option Premia. _Journal of Finance_, _33_, 129–147.

Schr¨oder M. (1989). Computing the Constant Elasticity of Variance Option Pricing Formula. _Journal of Finance_, _44_, 211–219.

Shimko D. (1991). _Finance in Continuous Time: A Primer_. Kolb Publishing Company.

Shu J., & Zhang J. (2004). Pricing S&P 500 Index Options Under Stochastic Volatility with the Indirect Inference Method. _Journal of Derivatives Accounting_, _1_, 1–16.

Simonato J.-G. (2011). Johnson Binomial Trees. _Quantitative Finance_, _11_, 1165–1176.

Smith C. (1976). Option Pricing: A Review. _Journal of Financial Economics_, _3_, 3–54.

Stentoft L. (2004). Convergence of the Least Squares Monte Carlo Approach to American Option Valuation. _Management Science_, _50_, 1193–1203.

Stoll H. (1969). The Relationship Between Put and Call Option Prices. _Journal of Finance_, _24_, 801–824.

Stulz R. (1982). Options on the Minimum or the Maximum of Two Risky Assets. _Journal of Financial Economics_, _10_, 161–185.

Tian Y. (1993). A Modified Lattice Approach to Option Pricing. _Journal of Futures Markets_, _13_, 563–577. Tian Y. (1999). A Flexible Binomial Option Pricing Model. _Journal of Futures Markets_, _19_, 817–843.

Toft K. (1996). On the Mean-Variance Trade-Off in Option Replication with Transaction Costs. _Journal of Financial and Quantitative Analysis_, _31_, 233–263.

Turnbull S., & Wakeman L. (1991). A Quick Algorithm for Pricing European Average Options. _Journal of Financial and Quantitative Analysis_, _26_, 377–389.

Widdicks M., Andricopoulos A., Newton D., & Duck P. (2002). On the Enhanced Convergence of Standard Lattice Methods for Option Pricing. _Journal of Futures Markets_, _22_, 315–338.

Wiggins J. (1987). Option Values under Stochastic Volatility: Theory and Empirical Estimates. _Journal of Financial Economics_, _19_, 351–372.

Wilmott P. (1994). Discrete Charms. _Risk_, _7_, 48–51.

Wilmott P. (2000). _Paul Wilmott on Quantitative Finance_. Wiley, Chichester.

1.  Implicitly, we assumed that as ∆_t →_ 0<sup>+</sup>, _S_(_t −_∆_t_) _→ S_(_t_), i.e., that the _S_ process is continuous. Empirically, this assumption appears to be a strong one; most asset returns appear to experience discontinuities also known as jumps. We will revisit the implications of these jumps much later in the book. [↑](#footnote-ref-1)
    
2.  To ease the notation, we drop the time dependency whenever it does not impede clarity. [↑](#footnote-ref-2)
    
3.  The result is also called the Itˆo-Doeblin formula in reference to French mathematician Wolfgang Doeblin whose independent derivation in 1940 was only discovered in 2000. [↑](#footnote-ref-3)
    
4.  If, over a year, _{R<sub>n</sub><sup>}</sup><sub>n</sub>_<sub>\=1</sub>_<sub>,...,N</sub>d_ were independent and identically distributed with variance _σ<sub>d</sub>_<sup>2</sup>, we would have _σ<sub>y</sub>_<sup>2</sup> \=
    
    Var <sup>P</sup>_<sup>N</sup>n_\=1_<sup>d</sup> R<sub>n</sub>_ \= <sup>P</sup>_<sup>N</sup><sub>n</sub>_<sub>\=1</sub>_<sup>d</sup>_ Var (_R<sub>n</sub>_) = _N<sub>d</sub>σ<sub>d</sub>_<sup>2</sup>, whence equation (3.8). [↑](#footnote-ref-4)
    
5.  Thus far, we denoted increments (e.g., in time) using ∆_t_. To better distinguish increments and the BMS greek ∆, we will here use _δt_ to denote increments. [↑](#footnote-ref-5)
    
6.  Note that if _S_ pays dividends at rate _y_ or has a convenience yield of _y_, _µ_ can be replaced by _µ − y_. [↑](#footnote-ref-6)
    
7.  Formally speaking, deriving the unconditional variance above requires this condition. [↑](#footnote-ref-7)
    
8.  In the original paper, and many that followed, the convexity correction is not explicit. That is
    
    _rt_+1 = _rf_ \+ _λhnht_+1 + p_ht_+1_εt_+1_._
    
    This implies a translation of the risk premium parameter, i.e., _λ<sub>hn</sub>_ \= _λ −_. Both formulations are thus observationally equivalent. However, some authors find _−_0_._5 _< λ<sub>hn</sub> <_ 0 and erroneously conclude that the model implies a negative risk premium. Explicitly accounting for the convexity correction clarifies the role played by _λ_. [↑](#footnote-ref-8)
    
9.  The _θ_ \= 3_/_2 case is investigated by Heston (1997). [↑](#footnote-ref-9)