The Pathfinder API allows you to find the shortest path between nodes in a graph. Such graph could be anything, for instance the map in an online game or the sitemap of an webpage.

**Note:** The Pathfinder API will likely be renamed one day, as we want to group it with other algorithms.

## Table of Contents

[TOC]

## PathFinder methods

##### `PathFinder.findShortestPath(graph, start_node, dest_node);`

- `graph` (object): The graph (See description)
- `start_node` (string): Name of the start node
- `dest_node` (string): Name of the destination node

Internally this method uses [Dijkstra's algorithm](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm) to find the shortest path from the `start_node` to the `dest_node` in a `graph`.

###### Graph Example:

**Note:** Each edges destination node must exist as a node. If a node does not exist, the method doesn't report it (yet).

```javascript

var graph = {
	north_adams: {
		greenfield: 38,
		pittsfield: 22
	},
	pittsfield: {
		north_adams: 22,
		lee: 12
	},
	lee: {
		pittsfield: 12,
		springfield: 41
	},
	springfield: {
		lee: 41,
		northampton: 19,
		worcester: 55
	},
	northampton: {
		springfield: 19,
		greenfield: 21
	},
	greenfield: {
		north_adams: 38,
		northampton: 21,
		fitchburg: 49,
		worcester: 61
	},
	fitchburg: {
		greenfield: 49,
		worcester: 27
	},
	worcester: {
		fitchburg: 27,
		greenfield: 61,
		springfield: 55
	}
};

PathFinder.findShortestPath(graph, "north_adams", "worcester");
```

In this example `.findShortestPath` will return this array: `["north_adams", "greenfield", "worcester"]`.