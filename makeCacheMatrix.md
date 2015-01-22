makeCacheMatrix <- function(x = numeric()) {
  inv <- NULL
  set <- function(dat,a,b) x <<- matrix(dat,a,b)
  get <- function() x
  setinv <- function() inv <<- solve(x)
  getinv <- function() print(inv)
  list(set = set, get = get,
       setinv = setinv,
       getinv = getinv)
}
