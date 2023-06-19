### **Pies**

The goal of this is to create a set of functions that can draw isosceles triangles attached together in a pie shape, the math for it is a little difficult though.

### Isosceles
```python
def isosceles(t, r, angle): 
	"""
	Draws an icosceles triangle. 
	
	The turtle starts and ends at the peak, facing the middle      of the base. 
	
	t: Turtle 
	r: length of the equal legs 
	angle: half peak angle in degrees 
	""" 
	y = r * math.sin(angle * math.pi / 180) 
	t.rt(angle)
	t.fd(r) 
	t.lt(90+angle) 
	t.fd(2*y) 
	t.lt(90+angle) 
	t.fd(r) 
	t.lt(180-angle)
```
Isosceles takes a turtle object, a length of the equal legs and then half of the angle of the inner angle

Does math that I don’t fully understand but it makes an isosceles triangle

### Polypie
```python
def polypie(t, n, r): 
	"""
	Draws a pie divided into radial segments. 
	t: Turtle n: number of segments 
	r: length of the radial spokes 
	""" 
	angle = 360.0 / n 
	for i in range(n): 
		isosceles(t, r, angle/2) 
		t.lt(angle)
```
This take a turtle, a number of pie 'slices' or segments, and a length of the spokes

Basically just loops through the number of pie slices, creates the triangles then turns left before the next