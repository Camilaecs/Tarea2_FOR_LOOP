# Tarea2_FOR_LOOP
Tarea de for

### TAREA N°2 BIGDATA

############ EJERCICIO 1 ############

listaDocumentos <- list(c("mp","Juan","Christofer"),c("of","av01","ampr"),c("of","av01","ante"),
                        c("of","av08","arme"),c("of","av02","ante"),c("of","av07","ampr"),
                        c("of","av03","dape"),c("of","av01","meca"),c("of","av02","dape"),
                        c("mp","Antonia"),c("mp","Christian","Mario"),
                        c("mp","Jose","Pedro","Antonela"),c("of","av05","meca"),
                        c("of","av04","dape"),c("of","av02","arme"))

listaDocumentos

Totalmp <- 0
#TotalNiñosmp <- c()
TotalNiñosmp <- 0

######## CON FUNCION

CalculoMp <-  function(listaDocumentos){
  
for (categoria in listaDocumentos){
  if (categoria[1] == "mp"){
    Totalmp <- Totalmp + 1
    
    #TotalNiñosmp<- c(TotalNiñosmp,(length(categoria)-1))
    TotalNiñosmp <- TotalNiñosmp + (length(categoria)-1)
    
    if((length(categoria)-1)==3){
      
      mp3<-0
      mp3<-mp3+1
      print(paste("se cuenta con:", mp3, "lista de mp de 3 niños"))
      
    } else if((length(categoria)-1)==2){
      
      mp2<-0
      mp2<-(mp2+1)
      print(paste("se cuenta con:", mp2, "lista de mp de 2 niños"))
      
    } else {
      
      mp1<-0
      mp1<-mp1+1
      print(paste("se cuenta con:", mp1, "lista de mp de 1 niños"))
    }
  
  }
  
}
  return(TotalNiñosmp)}

CalculoMp(listaDocumentos)

######## SIN FUNCION

for (categoria in listaDocumentos){
  if (categoria[1] == "mp"){
    Totalmp <- Totalmp + 1
    
    #TotalNiñosmp<- c(TotalNiñosmp,(length(categoria)-1))
    TotalNiñosmp <- TotalNiñosmp + (length(categoria)-1)
    
    if((length(categoria)-1)==3){
      
      mp3<-0
      mp3<-mp3+1
      print(paste("se cuenta con:", mp3, "lista de mp de 3 niños"))
      
    } else if((length(categoria)-1)==2){
      
      mp2<-0
      mp2<-(mp2+1)
      print(paste("se cuenta con:", mp2, "lista de mp de 2 niños"))
      
    } else {
      
      mp1<-0
      mp1<-mp1+1
      print(paste("se cuenta con:", mp1, "lista de mp de 1 niños"))
    }
    
  }
  
}


print(paste("Existen", Totalmp,"listas de mp, y dentro de los mp, hay",TotalNiñosmp, "niños"))



############ EJERCICIO 2 ############


av01 <- c("av01")
av02 <- c("av02")
av03 <- c("av03")
av04 <- c("av04")
av05 <- c("av05")
av07 <- c("av07")
av08 <- c("av08")



for (categoria in listaDocumentos){
  
  if (categoria[1] == "of" && categoria[2] == av01){
    av01 <- c(av01, categoria[3])
    
  } else if (categoria[1] == "of" && categoria[2] == av02){
    av02 <- c(av02, categoria[3])
    
  } else if (categoria[1] == "of" && categoria[2] == av03){
    av03 <- c(av03, categoria[3])
    
  } else if (categoria[1] == "of" && categoria[2] == av04){
    av04 <- c(av04, categoria[3])
    
  } else if(categoria[1] == "of" && categoria[2] == av05) {
    av05 <- c(av05, categoria[3])
    
  } else if(categoria[1] == "of" && categoria[2] == av07) {
    av07 <- c(av07, categoria[3])
    
  } else if(categoria[1] == "of" && categoria[2] == av08) {
    av08 <- c(av08, categoria[3])
  }
  
} 
 

av01
av02
av03
av04
av05
av07
av08

############ EJERCICIO 3 ############

TotalOF <- 0
aprobados <- 0
rechazados <- 0

for (categoria in listaDocumentos){
  
 if (categoria[1] == "of" ){
   TotalOF <- TotalOF + 1
   
  if(categoria[3] == "meca" ||categoria[3] == "arme"||categoria[3] == "ampr"){
    
    print(paste(categoria[2], "esta rechazado"))
    aprobados <- aprobados + 1
    
  } else {
    
    print(paste(categoria[2], "esta aprobado"))
    rechazados <- rechazados + 1
  }
   }
  }

print(paste("Existen en total:", TotalOF, "oficios, de los cuales", aprobados, "estan aprobados y", rechazados, "estan rechazados"))

