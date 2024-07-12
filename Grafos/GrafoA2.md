import matplotlib.pyplot as plt

# Creamos un grafo vacío
grafo = {}

# Agregamos vertices al grafo
grafo["A"] = ["B", "C"]
grafo["B"] = ["D"]
grafo["C"] = ["D"]
grafo["D"] = []

# Graficamos el grafo
fig, ax = plt.subplots()

vertices = list(grafo.keys())
for i, vertice in enumerate(vertices):
    for adyacente in grafo[vertice]:
        j = vertices.index(adyacente)
        ax.plot([i, j], [0, 1], "b-", linewidth=2)
        ax.text((i + j) / 2, 0.5, vertice + " -> " + adyacente, ha="center", va="bottom", fontsize=10)

ax.set_xlim(-0.5, len(vertices) - 0.5)
ax.set_ylim(-0.5, 1.5)
ax.set_xticks(range(len(vertices)))
ax.set_xticklabels(vertices)
ax.set_yticks([])
ax.set_title("Grafo dirigido")

plt.show()