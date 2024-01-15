import random
import os

import pygame
from pygame.constants import QUIT,K_DOWN,K_UP,K_RIGHT,K_LEFT

pygame.init()

FPS = pygame.time.Clock()
HEIGHT = 800 
WIDTH = 1200

FONT = pygame.font.SysFont('Verdana', 20)
 
COLOR_WHITE = (255, 255, 255)
COLOR_BLACK = (0, 0, 0)
COLOR_BLUE = (0, 0, 255)
COLOR_GREEN = (0, 255, 0)

main_display = pygame.display.set_mode((WIDTH, HEIGHT))

bg = pygame.transform.scale(pygame.image.load("background.png"),(WIDTH, HEIGHT))
bg_X1 = 0
bg_X2 = bg.get_width()
bg_move = 3

IMAGE_PATH = "Goose"
PLAYER_IMAGES = os.listdir(IMAGE_PATH)

player_size = (20, 20)
player = pygame.image.load("player.png").convert_alpha()  #pygame.Surface(player_size)
#player.fill(COLOR_BLACK)
player_rect = pygame.Rect(200,  300, *player_size)
# Coordinates in list below [x,y]
#player_speed = [1, 1]
player_move_down = [0,4]
player_move_up = [0,-4]
player_move_right = [4,0]
player_move_left = [-4,0]

def create_enemy():
    enemy_size = (100, 30)
    enemy = pygame.image.load("enemy.png").convert_alpha() #pygame.Surface(enemy_size)
    #enemy.fill(COLOR_BLUE)
    # We can use * to unpack collection - tuple, list. As below *enemy_size it put elements of tuple inside function 30,30
    enemy_rect = pygame.Rect(WIDTH, random.randint(30, HEIGHT-30), *enemy_size)
    enemy_move = [random.randint(-8, -4), 0]
    return [enemy, enemy_rect, enemy_move]

def create_bonuse():
    bonuse_size = (50, 200)
    bonuse = pygame.image.load("bonus.png").convert_alpha() #pygame.Surface(bonuse_size)
    #bonuse.fill(COLOR_GREEN)
    # We can use * to unpack collection - tuple, list. As below *enemy_size it put elements of tuple inside function 30,30
    bonuse_rect = pygame.Rect(random.randint(100, WIDTH-100), -HEIGHT, *bonuse_size)
    bonuse_move = [0,random.randint(4, 8)]
    return [bonuse, bonuse_rect, bonuse_move]


CREATE_ENEMY = pygame.USEREVENT + 1
pygame.time.set_timer(CREATE_ENEMY,1500)
CREATE_BONUSE = pygame.USEREVENT + 2
pygame.time.set_timer(CREATE_BONUSE,2000)
CHANGE_IMAGE = pygame.USEREVENT + 3
pygame.time.set_timer(CHANGE_IMAGE, 200)

enemies = []
bonuses = []

score = 0

image_index = 0


playing = True

while playing:
    FPS.tick(60)
    for event in pygame.event.get():
        if event.type == QUIT:
            playing = False
        if event.type == CREATE_ENEMY:
            enemies.append(create_enemy())
        if event.type == CREATE_BONUSE:
            bonuses.append(create_bonuse())
        if event.type == CHANGE_IMAGE:
            player = pygame.image.load(os.path.join(IMAGE_PATH, PLAYER_IMAGES[image_index]))
            image_index += 1
            if image_index >= len(PLAYER_IMAGES):
                image_index = 0
    
    #main_display.fill(COLOR_BLACK) 
    bg_X1 -= bg_move
    bg_X2 -= bg_move
    
    if bg_X1 < -bg.get_width():
        bg_X1 = bg.get_width()
        
    if bg_X2 < -bg.get_width():
        bg_X2 = bg.get_width()
    
    
    main_display.blit(bg, (bg_X1, 0))
    main_display.blit(bg, (bg_X2, 0))

    
    keys = pygame.key.get_pressed()
    if keys[K_DOWN] and player_rect.bottom < HEIGHT:
        player_rect = player_rect.move(player_move_down)
        
    if keys[K_UP] and player_rect.top >= 0:
        player_rect = player_rect.move(player_move_up)
    
    if keys[K_RIGHT] and player_rect.right < WIDTH:
        player_rect = player_rect.move(player_move_right)
        
    if keys[K_LEFT] and player_rect.left >= 0:
        player_rect = player_rect.move(player_move_left)
      
    for enemy in enemies:
        enemy[1] = enemy[1].move(enemy[2])
        main_display.blit(enemy[0], enemy[1])
        
        if player_rect.colliderect(enemy[1]):
            playing = False
    
    for bonuse in bonuses:
        bonuse[1] = bonuse[1].move(bonuse[2])
        main_display.blit(bonuse[0], bonuse[1])
        
        if player_rect.colliderect(bonuse[1]):
            score += 1
            bonuses.pop(bonuses.index(bonuse))
        
        
    #enemy_rect = enemy_rect.move(enemy_move)
    
    # if player_rect.bottom >= HEIGHT:
    #     player_speed[1] = -player_speed[1] 
        
    # if player_rect.right >= WIDTH:
    #     player_speed[0] = -player_speed[0]
        
    # if player_rect.top < 0:
    #     player_speed[1] = -player_speed[1]
        
    # if player_rect.left < 0:
    #     player_speed[0] = -player_speed[0]
        
    
        
    main_display.blit(FONT.render(str(score),True, COLOR_BLACK),(WIDTH - 50, 20))
    main_display.blit(player,player_rect)
    
    #main_display.blit(enemy, enemy_rect)
    
    #player_rect = player_rect.move(player_speed)
    
    pygame.display.flip()
    
    
    
    for enemy in enemies:
        if enemy[1].left <0:
            enemies.pop(enemies.index(enemy))
           
        
            
            
    for bonuse in bonuses:
        if bonuse[1].bottom >= HEIGHT:
            bonuses.pop(bonuses.index(bonuse))
        
        
            