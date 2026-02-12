

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









# Paired T-Test Program

# First sample (Before)
x <- c(10, 12, 15, 18)

# Second sample (After)
y <- c(8, 11, 14, 17)

# Perform paired t-test
result <- t.test(x, y, paired = TRUE)

cat("----- Paired T-Test Result -----\n")
print(result)

# Conclusion
if(result$p.value < 0.05){
  cat("\nConclusion: Reject Null Hypothesis\n")
  cat("There is a significant difference between the two paired samples.\n")
} else {
  cat("\nConclusion: Accept Null Hypothesis\n")
  cat("There is no significant difference between the two paired samples.\n")
}
