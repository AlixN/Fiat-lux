#Makefile for generating rendu1.x

#Definitions

CC      = gcc
CFLAGS  = -Wall
CFILES  = main.c absorbeur.c error.c modele.c photon.c projecteur.c reflecteur.c utilitaire.c

OFILES = $(CFILES:.c=.o) 

rendu1.x: $(OFILES)
	$(CC) $(OFILES) -lm -o rendu1.x
    
depend:
	@echo " *** MISE A JOUR DES DEPENDANCES ***"
	@(sed '/^# DO NOT DELETE THIS LINE/q' Makefile && \
        	$(CC) -MM $(CFLAGS) $(CFILES) | \
        	egrep -v "/usr/include" \
        	) > Makefile.new
	@mv Makefile.new Makefile
    
clean:
	@echo " *** MODULES OBJETS ET EXECUTABLES EFFACE ***"
	@/bin/rm -f *.o *.x *.c~ *.h~
    
###Règles automatiques
#
#
# DO NOT DELETE THIS LINE

main.o: main.c 


