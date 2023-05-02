# Intro_DS_HW4

#Exercice 3

pckg <- c ('ggplot2','ggforce')

install.packages('ggforce')
#load several packages at once
lapply(pckg, require, character.only = TRUE)


gg_circles <- function(){
  
  # construction of the plot
  ggplot() + geom_circle(aes(x0 = 0, y0 = 0, r =200 ), fill = "grey", color = "grey") +
    geom_circle(aes(x0 = -300, y0 = 300, r = 20), fill = "red", color = "red") +
    geom_circle(aes(x0 = 0, y0 = -300, r = 20), fill = "blue", color = "blue") +
    geom_circle(aes(x0 = 300, y0 = 300, r = 20), fill = "green", color = "green") +
    geom_text(aes(x=100,y=-300,label ='Satellite 2'))+
    geom_text(aes(x=-210,y=300,label ='Satellite 1'))+
    geom_text(aes(x=210,y=300,label ='Satellite 3'))+
    geom_text(aes(x=-190,y=-200,label ='Flat Earth'))+
    # define graph boarders
    coord_cartesian(xlim = c(-350, 350), ylim = c(-350, 350)) +
    # name axis
    xlab("x") + ylab("y")
}

gg_circles()
