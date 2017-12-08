# pong

import pygame, sys
from pygame.locals import *

fps = 150
screenheight = 450
screenwidth = 350

	
def mainfunc():
	pygame.init()
	global DISPLAYSURF
	
	fpsclock = pygame.time.Clock()
	DISPLAYSURF = pygame.display.set_mode((screenwidth,screenheight))
	pygame.display.set_caption("Pong!")
	
	while True:
		for event in pygame.event.get():
			if event.type == quit:
				pygame.quit()
				sys.exit()
				
		fpsclock.tick(fps)
		pygame.display.update()

		
if __name__=="__main__":
	mainfunc()
