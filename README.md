import pygame
import os
import time
import random
pygame.font.init()

WIDTH, HEIGHT = 750, 750
WIN = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Space Shooter")

# Load images
RED_SPACE_SHIP = pygame.image.load(os.path.join("assests", "pixel_ship_red_small.png"))
GREEN_SPACE_SHIP = pygame.image.load(os.path.join("assests", "pixel_ship_green_small.png"))
BLUE_SPACE_SHIP = pygame.image.load(os.path.join("assests", "pixel_ship_blue_small.png"))

# Player ship
YELLOW_SPACE_SHIP = pygame.image.load(os.path.join("assests", "pixel_ship_yellow_small.png"))

# Lasers
RED_LASER = pygame.image.load(os.path.join("assests", "pixel_laser_red_.png"))
GREEN_LASER = pygame.image.load(os.path.join("assests", "pixel_laser_green_.png"))
BLUE_LASER = pygame.image.load(os.path.join("assests", "pixel_laser_blue_.png"))
YELLOW_LASER = pygame.image.load(os.path.join("assests", "pixel_laser_yellow_.png"))

# Background
BG = pygame.transform.scale(image.load(os.path.join("assests", "background-black.png")), (WIDTH, HEIGHT))

def main():
    run = True
    FPS = 60
    level = 1
    lives = 5
    main_font = pygame.font.SysFont("comicsans", 50)
    
    clock = pygame.time.Clock()

def redraw_window():
    WIN.blit(BG, (0,0))
    # draw text
    lives_label = main_font.render(f"Lives: {lives}", 1, (255,255,255))
    level_label = main_font.render(f"Level: {level}", 1, (255,255,255))

    
    WIN.blit(lives_label, (10, 10))
    WIN.blit(level_label, (WIDTH - level_label.get_width() - 10, 10))
    pygame.display.update()
    
    while run:
        clock.tick(FPS)
        redraw_window()
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                run = False


main()
