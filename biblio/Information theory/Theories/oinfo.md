# Theory behind O-info
#OInfo #Multiplets #InformationTheory #IT #Theory #PID

## Mutual information
---

- Mutual information between two variables :
$$I(X; Y) = H(X) - H(X|Y)$$

- Conditional mutual information :
$$
\begin{equation}
	\begin{split}
		I(X; Y| Z) &= I(X; Y, Z) - I(X; Z) \\
		           &= I(X; Y) - I(X; Z) - I(X; Z|Y) \\
	\end{split}
\end{equation}
$$

## Interaction information
---
### Formula in terms of mutual-information

![[hoi_three_variables.png]]
For three variables :
- **Green :** $H(Z)$
- **Red :** $H(X)$
- **Blue :** $H(Y)$
Then :
$$
\begin{equation}
	\begin{split}
		I(X; Y; Z) &= I(X; Y) - I(X, Y | Z)
	\end{split}
\end{equation}
$$

### Link with the PID

![[pid_three_variables.png]]

- $I(X; Z) = Un_{X}(Z) + Red(X, Y |Z)$

$$
\begin{equation}
	\begin{split}
		I(X; Y; Z) &= I(X; Y) - I(X, Y | Z)
	\end{split}
\end{equation}
$$

## O-info
---

- **Formula of the O-info :**
$$
\begin{equation}
	\begin{split}
		\Omega(X^{n}) &= TotalCorrelation(TC) - DualTotalCorrelation(DTC) \\
		       &= C(X^{n}) - B(X^{n})
	\end{split}
\end{equation}
$$
- **Total Correlation (TC) :** $C(X^{n}) = \sum_{j=1}^{n}H(X_{j}) - H(X^{n})$ 
	- $\sum_{j=1}^{n}H(X_{j})$
		- *Total information carried by individual node*
		- *It can't be exceeded*. Therefore : $\sum_{j=1}^{n}H(X_{j}) \geq H(X^{n})$
	- $H(X^{n})$
		- Information carried by *individual nodes + their interactions*
		- If all variables $X$ are independent, then : $H(X^{n})=\sum_{j=1}^{n}H(X_{j})$ and therefore $C(X^{n})=0$
	- Since $H(X^{n})$ is necessarily smaller, $C(X^{n}) \geq 0$ 
	- *The difference between the two terms quantify the amount of redundant information shared between individual nodes*
- **Dual Total Correlation (DTC) :** $B(X^{n}) = H(X^{n}) - \sum_{j=1}^{n}H(X_{j}|X_{-j}^{n})$
	- $\sum_{j=1}^{n}H(X_{j}|X_{-j}^{n})$
		- Contribution of individual nodes once we remove the contribution of triplets, quadruplets etc.
		- This quantity is necessarily smaller than $H({X^{n}})$
	- The subtraction between the two terms *encapsulates the information contained in the interactions within multiplets exceeding the information of individual nodes (=synergy)*

$$
\begin{equation}
	\begin{split}
		\Omega(X^{n}) &= C(X^{n}) - B(X^{n}) \\
		              &= [\sum_{j=1}^{n}H(X_{j}) - H(X^{n})] - [H(X^{n}) - \sum_{j=1}^{n}H(X_{j}|X_{-j}^{n})] \\
		              &= -2H(X^{n}) + \sum_{j=1}^{n}H(X_{j}) + \sum_{j=1}^{n}H(X_{j}|X_{-j}^{n}) \\
		              &= -2H(X^{n}) + \sum_{j=1}^{n}H(X_{j}) + \sum_{j=1}^{n}H(X_{j}, X_{-j}^{n}) - \sum_{j=1}^{n}H(X_{-j}) \\
		              &= -2H(X^{n}) + nH(X^{n}) + \sum_{j=1}^{n}(H(X_{j})-H(X_{-j})) \\
		              &= (n-2)H(X^{n}) + \sum_{j=1}^{n}(H(X_{j})-H(X_{-j}))
		              
	\end{split}
\end{equation}
$$
