# Portfoliio
## Pre-Processing 
```
import pandas as pd
import matplotlib.pyplot as plt


df = pd.read_csv('./global-data-on-sustainable-energy(1).csv')


wanted = {"United States", "Canada", "United Kingdom"}


sub = df[df["Entity"].isin(wanted)]


pivot = sub.pivot(index="Year", columns="Entity", values="gdp_growth").sort_index()

plt.figure()  
for ent in pivot.columns:
    plt.plot(pivot.index, pivot[ent], marker="o", label=ent)

plt.title("gdp_growth over time — selected entities")
plt.xlabel("Year")
plt.ylabel("gdp_growth(%)")
plt.legend()
plt.grid(True, alpha=0.3)
plt.tight_layout()
plt.show()


import pandas as pd
import matplotlib.pyplot as plt


wanted = {"United States", "Canada", "United Kingdom"}


sub = df[df["Entity"].isin(wanted)]


pivot = sub.pivot(index="Year", columns="Entity", values="Renewable energy share in the total final energy consumption (%)").sort_index()

plt.figure()  
for ent in pivot.columns:
    plt.plot(pivot.index, pivot[ent], marker="o", label=ent)

plt.title("Renewable energy share in the total final energy consumption (%) over time")
plt.xlabel("Year")
plt.ylabel("Renewable energy share(%)")
plt.legend()
plt.grid(True, alpha=0.3)
plt.tight_layout()
plt.show()
```

## Graphs 
![alt text](https://github.com/AnshukGottipati/AnshukGottipati.github.io/blob/68c5c112904bb44eeeb9d6059ff1fe66eda14c94/graph1.png?raw=true)
![alt text](https://github.com/AnshukGottipati/AnshukGottipati.github.io/blob/68c5c112904bb44eeeb9d6059ff1fe66eda14c94/graph2.png?raw=true)
