# two player chess in python with Pygame!
# part one, set up variables images and game loop

import pygame

pygame.init()
WIDTH = 1000
HEIGHT = 900
screen = pygame. display.set_mode([WIDTH, HEIGHT])
pygame .display.set_caption ('Two-Player Pygame Chess!')
font = pygame. font. Font('freesansbold. ttf', 20)
big_font = pygame. font. Font('freesansbold.ttf', 50)
timer = pygame. time. Clock()
fps = 60
# game variables and images
white_pieces = ['rook', 'knight', 'bishop', 'king', 'queen', 'bishop', 'knight', 'rock', 'pawn',
                'pawn', 'pawn', 'pawn', 'pawn', 'pawn', 'pawn', 'pawn']
white_locations = [(0, 0), (1, 0), (2, 0), (3, 0), (4, 0), (5, 0), (6, 0), (7, 0),
                   (0, 1), (1, 1), (2, 1), (3, 1), (4, 1), (5, 1), (6, 1), (7, 1)]
black_pieces = ['rook', 'knight', 'bishop', 'king', 'queen', 'bishop', 'knight', 'rook'
                'pawn', 'pawn', 'pawn', 'pawn', 'pawn', 'pawn', 'pawn', 'pawn']
black_locations = [(0, 7), (1, 7), (2, 7), (3, 7), (4, 7), (5, 7), (6, 7), (7, 7),
                   (0, 6), (1, 6), (2, 6), (3, 6), (4, 6), (5, 6), (6, 6), (7, 6)]
captured_pieces_white = []
captured_pieces_black = []
# 0 - whites turn no selection: 1-whites turn piece selected: 2- black turn no selection, 3 - black turn piece selected
turn_step = 0
selection = 100
valid_moves = []
# Load in game piece images (queen, king, rook, bishop, knight, pawn) x 2
black_queen = pygame. image. load('assets/images/black queen.png')
black_queen = pygame. image. scale(black_queen, (80, 80))
black_queen_small = pygame.image.scale (black_queen, (45, 45))
