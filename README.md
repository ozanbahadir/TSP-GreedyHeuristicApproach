# TSP-GreedyHeuristicApproach
# The following are all the methods and data used for the code:

Class name:	Nearest_Neighbor
Methods:
●	mark_unvisited_cities: Marks all cities unvisited by resetting the list of coordinates and vertices”
●	empty_tour: Clears all the edges of the current tour”
●	calculate_nearneighbor: Pre: takes in a list of all unvisited vertices, and update the nearest city and cost of travelling to the nearest city”
●	mark_visited: Takes in a  list of all unvisited cities, pops current city from list of vertices and labels
●	add_currcity_tour(): Creates an edge between current city and nearest city and adds that to the best tour graph
●	add_tourCost(): Takes in the cost of travelling the last city, and updates the  total tour cost by adding the cost of visiting the last city

Data:
●	cost_of_best_tour_so_far: sets cost of best tour to infinity initially
●	cost_of_tour: cost of one tour
●	labels: a list containing all the labels of the vertices
●	best_label: a list containing all the labels for for a given tour 
●	best_label_so_far: a list containing all the labels for the best possible tour
●	all_coordinates = coordinates:  list containing all the given coordinates
●	coordinates = []: a list containing the deep copy of the given coordinates
●	best_coordinates = []: a list containing the coordinates in the order of travel for a given tour
●	best_coordinates_so_far = []: a list containing the coordinates in the order of travel for the best possible tour
●	unvisited_cities = []: a list containing all the unvisited cities(list of Vertex objects)
●	vertices = [Vertex(c) for c in self.labels]: a list of all the cities generated using all the labels
●	best_tour = Graph(self.vertices): a graph object containing a given tour
●	self.best_tour_so_far = Graph(self.vertices): a graph object containing the best tour so far
●	self.currentcity = None: Vertex object to contain the current city
●	self.currentcity_coordinate = (): a tuple containing the coordinates for the current city
●	self.startcity = None : Vertex containing the start city
●	self.nearestcity = None: Vertex containing the nearest city
●	self.cost_to_nearest_city = float('inf'): Cost of travelling to the nearest city	

Class name:	TspRW

Methods:
●	read_file(): take is an ASCII file where each line will be the vertex number, x-coordinate, and y-coordinate separated by spaces and updates self.labels and self.coordinates by extracting the labels from the ASCII file
●	write_file(): Writes an ASCII file where each line contains the number of a single vertex listed in the order of the tour
Data:
●	self.header = []:  a list containing the header section of the file
●	self.labels = ls:  a list containing all the labels of vertices
●	self.coordinates = cd: a list containing all the coordinates of vertices
●	self.filename = 0 :  the input file name	●	 

Design for main() file:
____________________________________________________________
Asks the user to input a filename to find vertices 
Reads all the coordinates of vertices from the file
Create a list of vertices 
Create a list of coordinates
For each vertex do the following
●	Mark all cities unvisited 
●	Empties the tour
●	Set the vertex to start city
●	Sets the start city to current city
●	Marks the city visited
●	While there is an unvisited city do the following:
○	Find and calculate the distance from the starting node to nearest node
○	Add the nearest city to the tour
○	Add the cost to the tour cost
○	Assign current city to be the nearest city
○	Marks the current city visited
○	Creates the last edge between the current and start city and adds that to the tour
●	   Updates the best tour so far if the last tour was less costly
Once all the cities have been visited, 
Write the best tour’s coordinates to an ASCII file with .tour extension
Call the GraphWorld to draw the graph	Imports the following classes: TspRW,GraphWorld, Graph, Nearest_Neighbour
 
