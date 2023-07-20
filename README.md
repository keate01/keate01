from PIL import Image, ImageDraw

# Créer une image vierge pour la photo de profil (taille 200x200 pixels)
profile_image = Image.new("RGB", (200, 200), color=(255, 255, 255))

# Dessiner un cercle pour simuler une photo de profil
draw = ImageDraw.Draw(profile_image)
draw.ellipse((10, 10, 190, 190), fill="blue", outline="black", width=2)

# Sauvegarder l'image de profil
profile_image.save("profile_image.jpg")

# Créer une image vierge pour la couverture (taille 1080x360 pixels)
cover_image = Image.new("RGB", (1080, 360), color=(255, 255, 255))

# Dessiner un texte sur la couverture
draw = ImageDraw.Draw(cover_image)
font_size = 50
text = "Côte d'Ivoire la Belle"
text_width, text_height = draw.textsize(text)
x = (1080 - text_width) // 2
y = (360 - text_height) // 2
draw.text((x, y), text, fill="black", font=("Arial", font_size))

# Sauvegarder l'image de couverture
cover_image.save("cover_image.jpg")
