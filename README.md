

x<-c(20,13,15,16)
mu<-mean(x)
sigma<-sqrt(sum((x-mu)^2)/length(x))
cat("mean is ",mu)
cat("sigma",sigma)









# Sample data
x <- c(20,13,15,16)

# Hypothesized population mean
mu0 <- 15

# Population standard deviation (given)
sigma <- 3

# Sample size
n <- length(x)

# Sample mean
xbar <- mean(x)

# Z statistic
z <- (xbar - mu0) / (sigma / sqrt(n))

# P-value (two tailed test)
p_value <- 2 * (1 - pnorm(abs(z)))

cat("Sample Mean =", xbar, "\n")
cat("Z value =", z, "\n")
cat("P-value =", p_value)









x <- c(20,13,15,16)

mu0 <- 15
n <- length(x)

xbar <- mean(x)
s <- sd(x)

t_value <- (xbar - mu0) / (s / sqrt(n))

cat("Sample Mean =", xbar, "\n")
cat("t value =", t_value)
