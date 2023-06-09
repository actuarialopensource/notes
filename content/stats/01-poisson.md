# Probability Models (Stochastic Processes and Survival Models)

## Properties of Poisson processes

### What is a Poisson process?

A Poisson process is a mathematical model used to describe a sequence of events that occur randomly in time or space. It is named after the French mathematician Siméon Denis Poisson and is widely used in various fields such as physics, engineering, biology, and finance.

The main characteristics of a Poisson process are:

1. The number of events occurring in non-overlapping intervals is independent. This means that the occurrence of an event in one interval does not affect the probability of events occurring in any other interval.
2. The average rate of events (usually denoted as λ, called intensity or rate) is constant over time or space. This rate represents the average number of events that occur in a unit of time or space.
3. The probability of more than one event occurring in an infinitesimally small interval or region approaches zero as the interval or region becomes smaller.

A Poisson process is often used to model random events such as phone calls arriving at a call center, radioactive decay of atoms, or customers arriving at a queue. The Poisson distribution, a discrete probability distribution, is derived from the Poisson process and describes the probability of a given number of events occurring in a fixed interval of time or space.

### What is a non-homogenous Poisson process?

A non-homogeneous Poisson process, also known as an inhomogeneous or non-stationary Poisson process, is a generalization of the Poisson process where the event rate (intensity) is allowed to vary over time or space. In a standard Poisson process, the event rate is constant, but in a non-homogeneous Poisson process, the event rate can change as a function of time or space.

The main characteristics of a non-homogeneous Poisson process are:

1. The number of events occurring in non-overlapping intervals is independent, just like in a homogeneous Poisson process.
2. The event rate (intensity) λ(t) is no longer constant but is a function of time (or space). This means that the average number of events can change over time or space.
3. The probability of more than one event occurring in an infinitesimally small interval or region still approaches zero as the interval or region becomes smaller.

Non-homogeneous Poisson processes are used to model situations where the rate of events varies over time or space, such as the number of earthquakes in a region over time, the intensity of rainfall in different seasons, or the arrival of customers at a store during different hours of the day.

### The memoryless property of exponential and Poisson distributions

The memoryless property is a characteristic of certain probability distributions, specifically the exponential distribution for continuous random variables and the Poisson distribution for discrete random variables. This property essentially means that the probability of an event occurring in the future is independent of how long it has been since the last event.

For the exponential distribution, the memoryless property can be stated mathematically as follows:

P(X > t + s | X > s) = P(X > t)

Here, X is a continuous random variable following an exponential distribution, and t and s are positive values. The equation states that the probability of the event not occurring until after time t+s, given that it has not occurred by time s, is equal to the probability of the event not occurring until after time t.

For the Poisson distribution, the memoryless property can be expressed mathematically as:

P(N(t + s) - N(s) = k) = P(N(t) = k)

Here, N(t) is a discrete random variable representing the number of events occurring by time t in a Poisson process, and k is a non-negative integer. The equation states that the probability of observing k events in the interval (s, t+s], given that no events occurred in the interval (0, s], is equal to the probability of observing k events in the interval (0, t].

The memoryless property has important implications for modeling real-world phenomena. It allows us to make predictions about future events based only on the current state, without needing to consider the history of past events. This property makes the exponential and Poisson distributions suitable for modeling situations where the timing of events is random and independent, such as radioactive decay, customer arrivals, or phone call durations.

### Relationship between exponential and Gamma

The exponential and gamma distributions are both continuous probability distributions used to model different types of random processes. They are closely related, as the exponential distribution is a special case of the gamma distribution.

The gamma distribution is characterized by two parameters: a shape parameter (k or α) and a scale parameter (θ or β). Its probability density function (PDF) is given by:

f(x; α, β) = (1 / (β^α * Γ(α))) * x^(α - 1) * e^(-x/β), for x > 0, α > 0, and β > 0,

where Γ(α) is the gamma function, a generalization of the factorial function.

The exponential distribution is characterized by a single parameter: the rate (λ) or its reciprocal, the mean (μ). Its PDF is given by:

f(x; λ) = λ * e^(-λx), for x > 0 and λ > 0.

The relationship between the gamma and exponential distributions is that the exponential distribution is a special case of the gamma distribution when the shape parameter (α) is equal to 1. In other words, if we set α = 1 and β = 1/λ in the gamma distribution's PDF, we obtain the exponential distribution's PDF:

f(x; 1, 1/λ) = (1 / (1/λ)) * x^(1 - 1) * e^(-λx) = λ * e^(-λx).

This connection means that the exponential distribution can be seen as a gamma distribution with a shape parameter of 1. The gamma distribution provides a more general framework to model various types of random processes with different shapes and scales, while the exponential distribution is specifically suited for modeling memoryless processes with a constant rate of occurrence.

### Relationship between exponential and Poisson

The relationship between the exponential and Poisson distributions lies in their connection to the Poisson process, a model used to describe the random occurrence of events in time or space. While the Poisson distribution models the number of events in a fixed interval, the exponential distribution models the time between consecutive events.

Here's a summary of their roles in the context of a Poisson process:

Poisson distribution: The Poisson distribution is a discrete probability distribution that models the number of events occurring in a fixed interval of time or space, given a constant average rate of events (λ). Its probability mass function (PMF) is given by:
P(X=k) = (e^(-λt) * (λt)^k) / k!, for k = 0, 1, 2, ...

Here, X represents the number of events in the interval, λ is the average event rate, and t is the length of the interval.

Exponential distribution: The exponential distribution is a continuous probability distribution that models the time (or distance) between consecutive events in a Poisson process, given a constant event rate (λ). Its probability density function (PDF) is given by:
f(x) = λ * e^(-λx), for x ≥ 0.

Here, x represents the time (or distance) between consecutive events, and λ is the average event rate.

In summary, the relationship between the exponential and Poisson distributions is that they are both connected to the Poisson process, with the Poisson distribution describing the number of events in a fixed interval and the exponential distribution describing the time (or distance) between consecutive events. The constant event rate (λ) is a common parameter that links these two distributions in the context of a Poisson process.

## Inter-arrival and waiting distributions associated with a Poisson process

### Sample calculations for Poisson

Example 1: Poisson Distribution
Suppose a call center receives an average of 10 calls per hour (λ = 10). What is the probability of receiving exactly 7 calls in an hour?

Using the Poisson distribution's probability mass function:

P(X=k) = (e^(-λt) * (λt)^k) / k!

We plug in the values λ = 10 (average calls per hour), t = 1 (one hour), and k = 7 (number of calls):

P(X=7) = (e^(-10) * (10)^7) / 7!
P(X=7) ≈ 0.0901

So, the probability of receiving exactly 7 calls in an hour is about 9.01%.

Example 2: Exponential Distribution
Now let's find the probability that the time between two consecutive calls is more than 10 minutes. First, convert 10 minutes to hours (10/60 = 1/6 hours). Recall that the average call rate is 10 calls per hour, so λ = 10.

Using the exponential distribution's cumulative distribution function (CDF), we can find the probability that the waiting time between calls is less than or equal to x:

F(x) = 1 - e^(-λx)

We want to find the complementary probability, which is the probability that the waiting time between calls is greater than x:

P(X > x) = 1 - F(x) = e^(-λx)

Plugging in the values λ = 10 and x = 1/6:

P(X > 1/6) = e^(-10 * 1/6)
P(X > 1/6) ≈ 0.0111

So, the probability of waiting more than 10 minutes between consecutive calls is about 1.11%.

These examples demonstrate how to use the Poisson and exponential distributions to make calculations in the context of a Poisson process. The first example calculates the probability of a specific number of events occurring in a fixed interval, while the second example calculates the probability of the time between consecutive events being greater than a specified value.

### Conditional distribution of arrival times

In the context of a Poisson process, the conditional distribution of arrival times refers to the distribution of event arrival times, given that a certain number of events have occurred in a specified time interval.

One important property of a Poisson process is that the conditional distribution of arrival times, given the number of events, is uniform over the interval. This property is a direct consequence of the independent increments property and the constant event rate of a homogeneous Poisson process.

To illustrate this with an example, let's consider a bus stop where buses arrive according to a Poisson process with an average rate of 2 buses per hour (λ = 2). Now, suppose we know that 3 buses will arrive between 9:00 AM and 10:00 AM. We are interested in finding the distribution of the arrival times of these buses, given this information.

Since the Poisson process has the property that the conditional distribution of arrival times, given the number of events, is uniform over the interval, we can conclude that the buses' arrival times are uniformly distributed between 9:00 AM and 10:00 AM, given that we know 3 buses will arrive during this period.

This uniform distribution implies that the probability of a bus arriving in any subinterval (e.g., between 9:15 AM and 9:30 AM) is proportional to the length of that subinterval. In other words, the buses are equally likely to arrive at any time between 9:00 AM and 10:00 AM, given the total number of arrivals in the interval.

It is important to note that this result is specific to a homogeneous Poisson process, where the event rate is constant over time. In a non-homogeneous Poisson process, the conditional distribution of arrival times may not be uniform, as the event rate can vary over time.

### Poisson splitting

Splitting a Poisson process into subsets of a population refers to partitioning the events in the process into different categories, based on some criteria or characteristic. When a Poisson process is split into subsets, the resulting processes for each subset are also Poisson processes, with event rates proportional to the probabilities associated with each category. This is known as the "Poisson Splitting" property.

Let's consider a Poisson process with rate λ, representing the total number of events occurring in a given time interval. Now, suppose each event can be classified into one of two distinct categories A and B. The probability of an event belonging to category A is p_A and to category B is p_B, such that p_A + p_B = 1.

When we split the original Poisson process based on these categories, we obtain two independent Poisson processes for categories A and B, each with rates λ_A = λ * p_A and λ_B = λ * p_B, respectively.

Let's illustrate this concept with an example:

Imagine a hospital emergency room where patients arrive according to a Poisson process with an average rate of 12 patients per hour (λ = 12). Patients can be classified into two categories: those with minor injuries (category A) and those with major injuries (category B). Suppose that the probabilities of a patient having a minor injury (p_A) and a major injury (p_B) are 0.75 and 0.25, respectively.

By applying the Poisson splitting property, we can derive separate Poisson processes for the arrivals of patients with minor and major injuries:

Minor injuries (Category A): λ_A = λ * p_A = 12 * 0.75 = 9 patients per hour.
Major injuries (Category B): λ_B = λ * p_B = 12 * 0.25 = 3 patients per hour.
Thus, after splitting the original Poisson process, we have two independent Poisson processes: one for patients with minor injuries, arriving at an average rate of 9 per hour, and another for patients with major injuries, arriving at an average rate of 3 per hour.

This concept can be extended to more than two categories or subsets, each with its own probability and corresponding Poisson process.

### Conditional distribution of events by category within a group within a certain time period

In the context of a Poisson process that has been split into categories (as discussed in the previous answer), the conditional distribution of events by category within a group and within a certain time period refers to the probability distribution of the number of events of a specific category, given the total number of events that occurred in that time period.

Let's consider a Poisson process split into categories A and B with probabilities p_A and p_B, and average rates λ_A and λ_B, respectively, within a given time period t. Suppose we know that there are n total events that occurred during this time period.

To compute the conditional distribution of events by category, we can use the binomial distribution. The reason for this is that once we know the total number of events (n), we are essentially interested in the number of "successes" (events of a specific category, say A) out of n trials, where each "success" occurs with probability p_A.

The probability mass function (PMF) of the binomial distribution is given by:

P(X=k) = C(n, k) * p^k * (1-p)^(n-k)

Here, X represents the number of successes (events of category A), C(n, k) denotes the number of combinations of n items taken k at a time (also written as "n choose k"), p is the probability of success (p_A), and k represents the number of successful events.

Using this PMF, we can calculate the probability of observing a specific number of events from each category within the time period, given the total number of events.

For example, suppose we have a Poisson process split into categories A and B with probabilities p_A = 0.6 and p_B = 0.4. We know that there are n = 10 events that occurred during a specific time period. To find the probability of exactly 7 events from category A and 3 events from category B, we would use the binomial distribution:

P(X=7) = C(10, 7) * (0.6)^7 * (0.4)^3 ≈ 0.215

So, there is approximately a 21.5% chance of observing 7 events from category A and 3 events from category B within the given time period, knowing that there are 10 events in total.

## Compound Poisson process, moments associated with the value of the process at a given time

### Compound Poisson process mean and variance

A compound Poisson process is a stochastic process that combines a Poisson process with another random process, typically involving random variables that represent the size or magnitude of the events. In a compound Poisson process, events occur according to a Poisson process with rate λ, and each event is associated with a random variable Y_i, which is independent and identically distributed (i.i.d.) according to some distribution F. The sum of the random variables associated with the events up to time t is represented by S(t).

To describe the mean and variance of a compound Poisson process, let's first define the mean (μ_Y) and variance (σ_Y^2) of the random variable Y:

μ_Y = E[Y]
σ_Y^2 = Var[Y]

Now, we can derive the mean and variance of the compound Poisson process S(t) at time t:

Mean of S(t):
E[S(t)] = λt * μ_Y

Variance of S(t):
Var[S(t)] = λt * (σ_Y^2 + μ_Y^2) - (λt * μ_Y)^2

These expressions show that the mean and variance of a compound Poisson process depend on the rate of the underlying Poisson process (λ), the time t, and the mean and variance of the random variable Y associated with each event.

In summary, a compound Poisson process combines a Poisson process with another random process, represented by random variables Y_i. The mean and variance of a compound Poisson process are determined by the rate of the Poisson process, the time, and the mean and variance of the random variables associated with the events.

### Normal approximation and hypothesis testing

In certain cases, the compound Poisson process can be approximated by a normal distribution. This approximation is particularly useful when the number of events is large, and it allows for easier calculations and hypothesis testing.

The Central Limit Theorem (CLT) states that the sum of a large number of independent and identically distributed random variables approaches a normal distribution, regardless of the original distribution of the variables. In the context of a compound Poisson process, the sum S(t) can be seen as a sum of random variables (each associated with an event), making the CLT applicable when the number of events is large.

To approximate a compound Poisson process with a normal distribution, you can use the mean and variance derived in the previous answer:

Mean: E[S(t)] = λt * μ_Y
Variance: Var[S(t)] = λt * (σ_Y^2 + μ_Y^2) - (λt * μ_Y)^2

A normal distribution is characterized by its mean (μ) and variance (σ^2), so we can approximate S(t) with a normal distribution N(μ, σ^2), where:

μ = E[S(t)] = λt * μ_Y
σ^2 = Var[S(t)]

For hypothesis testing, the normal approximation can be used to derive p-values or critical values for various statistical tests. For example, you can use a z-test to compare the mean of a compound Poisson process to a hypothesized value or to test the equality of means of two independent compound Poisson processes.

When using the normal approximation for a compound Poisson process, it is essential to ensure that the number of events is large enough for the approximation to be accurate. As a rule of thumb, the underlying Poisson process should have a sufficiently large rate (λt) and the distribution of the random variable Y should not be too skewed or heavy-tailed. Otherwise, the normal approximation may not provide reliable results for hypothesis testing.

## Poisson process concepts to calculate the hazard function and related survival model concepts.

When considering failure times in the context of a Poisson process, we typically examine the time between events, which is also known as the interarrival time. For a homogeneous Poisson process, the interarrival times are independent and identically distributed (i.i.d) according to an exponential distribution with a rate parameter λ, which is the average rate of the Poisson process.

In this context, the failure time represents the time it takes for a specific number of events to occur in the Poisson process. To find the distribution of the failure time, we can use the interarrival times' distribution and the properties of a Poisson process.

Let's consider T_k to be the failure time, representing the time until the k-th event occurs in a homogeneous Poisson process with rate λ. The failure time T_k can be represented as the sum of the first k interarrival times:

T_k = X_1 + X_2 + ... + X_k

Since the interarrival times (X_i) are i.i.d exponential random variables with rate λ, the sum T_k follows a Gamma distribution with shape parameter k and rate parameter λ:

T_k ~ Gamma(k, λ)

The probability density function (PDF) of the Gamma distribution is given by:

f(t) = (λ^k * t^(k-1) * exp(-λt)) / Γ(k) for t ≥ 0

where Γ(k) is the gamma function evaluated at k.

Now, we can use the Gamma distribution to derive the hazard function, cumulative hazard function, and survival function for the failure time T_k in a Poisson process:

Survival Function (S(t)):
S(t) = P(T_k > t) = 1 - P(T_k ≤ t) = 1 - F(t), where F(t) is the cumulative distribution function (CDF) of the Gamma distribution.

Hazard Function (h(t)):
h(t) = f(t) / S(t), where f(t) is the PDF of the Gamma distribution.

Cumulative Hazard Function (H(t)):
H(t) = -ln(S(t))

In summary, to analyze failure times in the context of a Poisson process, we consider the interarrival times' distribution, which is exponential for a homogeneous Poisson process. The failure time, representing the time until the k-th event occurs, follows a Gamma distribution with shape parameter k and rate parameter λ. The hazard function, cumulative hazard function, and survival function can be derived from the Gamma distribution and used to study the failure times in various applications.

## Joint distributions

TODO