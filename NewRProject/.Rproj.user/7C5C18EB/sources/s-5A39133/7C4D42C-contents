coches<- read.csv("~/Desktop/Ubiqum/coches.csv")
View(coches)
trainSize<-round(nrow(coches)*0.7) 
testSize<-nrow(coches)-trainSize
training_indices<-sample(seq_len(nrow(coches)),size =trainSize)
trainSet<-coches[training_indices,]
testSet<-coches[-training_indices,] 

linearMod <- lm(distance.of.car ~ speed.of.car, trainSet)
print(linearMod)
PredictionsName <- predict(linearMod,testSet)

boxplot(coches$speed.of.car, coches$distance.of.car
        )
