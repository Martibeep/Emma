from PIL import Image, ImageDraw, ImageFont

# Create a blank white image
img = Image.new('RGB', (800, 200), color=(255, 255, 255))

# Initialize the drawing context
d = ImageDraw.Draw(img)

# Use default font (built-in to Pillow)
font_big = ImageFont.load_default()
font_normal = ImageFont.load_default()

# Text positions
x_position = 50  # Starting X position
y_position = 40  # Y position for the text

# Draw the large red '1'
d.text((x_position, y_position), "1", fill=(255, 0, 0), font=font_big)
x_position += 50  # Adjust x_position after the big '1' to add the rest of the text

# Draw the rest of the text in normal size and black color
d.text((x_position, y_position + 20), "st KEY 〽️arkets", fill=(0, 0, 0), font=font_normal)

# Save the image
img.save("1st_key_markets.png")

# Show the image
img.show()