# assignment2


1) Make Cache matrix


makeCacheMatrix <- function(x = matrix()) {
  inv <- NULL
  set <- function(y){
    x <<- y
    inv <<- NULL
  }
  get <- function() x
  setInverse <- function(solveMatrix) inv <<- solveMatrix
  getInverse <- function() inv
  list(set = set, get = get, setInverse = setInverse, getInverse = getInverse)
}



2) cache solve


## This function computes the inverse of the special "matrix" returned by makeCacheMatrix above.
cacheSolve <- function(x, ...) {
  ## Return a matrix that is the inverse of 'x'
  inv <- x$getInverse()
  if(!is.null(inv)){
    message("getting cached data")
    
    
    
    or
    
    
    
    #base function
makeCacheMatrix <- function(x = matrix()) {
inverse <- NULL
set <- function(y) {
x <<- y
inverse <<- NULL
}
get <- function() {
print(x)
}
setinverse <- function(input){
inverse <<- input
}
getinverse <- function(){
print(inverse)
}
list(set = set, get = get,
setinverse = setinverse,
getinverse = getinverse)
}
Write a short comment describing this function
#the solve function
cacheSolve <- function(x, ...) {
Return a matrix that is the inverse of 'x'
inverse <- x$getinverse()
if(is.null(inverse)){
matrix <- x$get()
inverse <- solve(matrix)
x$setinverse(inverse)
}else{
return(inverse())
}
print(inverse)
}
#test
A <- makeCacheMatrix(matrix(1:9,3,3))
A$get()
A$getinverse()
A$set(matrix(c(2,0,0,3),2,2))
A$get()
cacheSolve(A)
A$getinverse()
    return(inv)
  }
  data <- x$get()
  inv <- solve(data)
  x$setInverse(inv)
  inv      
}
