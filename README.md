# reloj
y_position = 0
color_is = False
def setup():
    size(600,610)
    
def draw():
    global y_position 
    background(255)
    if color_is == True:
       fill(230, 0, 38)
    else:
       fill(100, 50, 187)

    ellipse(width /1.15, y_position, 100, 100)
    if y_position > height:
       y_position = 0
    else:
       y_position = map(second(), 0, 59, 0, height)


    ellipse(width / 5, y_position, 50, 50)
    if y_position > height:
       y_position = 0
    else:
       y_position = map(minute(), 0, 59, 0, height)
       
    ellipse(width / 1.85, y_position, 75, 75)
    if y_position > height:
       y_position = 0
    else:
       y_position = map(hour(), 0, 23, 0, height)