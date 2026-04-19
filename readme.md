# Spike Web Workers with Filesystem Protocol

A simple test to see how Web Workers work (or don't) when loaded from the filesystem and thus use the `file://` protocol. 

Right-click, Save As (computer) / "Share" (iOS): [web-worker-filesystem-spike.html](https://raw.githubusercontent.com/colinkershaw/web-worker-filesystem-spike/refs/heads/main/web-worker-filesystem-spike.html)

## Result
Web Workers seem to work just fine from the `file://` protocol in Chrome and Edge on Windows 11, and also Chrome and Edge on iOS (so WebKit, which should also cover Safari, but it wasn't an option to open the file in from Files app) .

## Prime Numbers

For testing your BigInt code, use these primes of varying scales. Note that because your code uses trial division ($O(\sqrt{n})$), the "Massive" numbers will definitely trigger your 10-second timeout safety net.
## 1. Small Primes (Instant Results)
These are ideal for verifying that your worker is communicating correctly.

* 7,919 (the 1,000th prime) [1][2]
* 104,729 (the 10,000th prime) [1, 2]
* 1,237 [3]

## 2. Medium Primes (Noticeable Delay)
These may take a few seconds depending on your device's CPU speed.

* 179,426,549 (A 9-digit prime; roughly 6–7 seconds on a standard brute-force script) [4]
* 999,999,999,999,989 (A 15-digit prime just under one quadrillion) [5]
* 9,007,199,254,740,881 (Your original 16-digit target; near the limit of 64-bit precision) [6]

## 3. Massive Primes (Guaranteed Timeout)
Trial division would take years for these; they are perfect for testing your safety net.

* 12,345,678,910,987,654,321 (A memorable 20-digit palindromic prime) [7]
* 10,000,000,000,000,666,000,000,000,000,001 (Belphegor's Prime; 31 digits) [8]
* 170,141,183,460,469,231,731,687,303,715,884,105,727 (A 39-digit Mersenne prime, $2^{127}-1$) [9, 10]


Sources:

- [1] [https://www.gleammath.com](https://www.gleammath.com/post/the-search-for-the-largest-primes-and-a-million-dollar-problem)
- [2] [https://inventwithpython.com](https://inventwithpython.com/cracking/chapter22.html#:~:text=Here%20is%20a%20short%20list%20of%20prime,269%2C%20271%2C%20277%2C%20281%2C%20and%20so%20on.)
- [3] [https://www.quora.com](https://www.quora.com/Whats-the-fastest-way-to-check-if-a-large-number-about-1024-bits-is-a-prime-number)
- [4] [https://medium.com](https://medium.com/swlh/the-prime-number-test-a-brute-force-approach-a25b9d6b231)
- [5] [https://prime-numbers.fandom.com](https://prime-numbers.fandom.com/wiki/999,999,999,999,989#:~:text=999%2C999%2C999%2C999%2C989%20is%20a%20prime%20number%20between%20999%2C999%2C999%2C999%2C000%20and%201%2C000%2C000%2C000%2C000%2C000.)
- [6] [https://prime-numbers.fandom.com](https://prime-numbers.fandom.com/wiki/9,007,199,254,740,881)
- [7] [https://www.scientificamerican.com](https://www.scientificamerican.com/article/these-prime-numbers-are-so-memorable-that-people-hunt-for-them/#:~:text=The%20number%2012%2C345%2C678%2C910%2C987%2C654%2C321%20is%20indeed%20prime.%20It,the%20number%20n%20and%20then%20descending%20again.)
- [8] [https://en.wikipedia.org](https://en.wikipedia.org/wiki/Palindromic_prime#:~:text=Due%20to%20the%20superstitious%20significance%20of%20the,one%20of%20the%20seven%20princes%20of%20Hell.)
- [9] [https://blogs.und.edu](https://blogs.und.edu/und-today/2025/06/integral-integers-why-prime-numbers-fascinate-mathematicians/#:~:text=The%20search%20for%20large%20primes%20Their%20work,equals%20170%2C141%2C183%2C460%2C469%2C231%2C731%2C687%2C303%2C715%2C884%2C105%2C727%2C%20and%20that%20value%20is%20prime.)
- [10] [https://blogs.und.edu](https://blogs.und.edu/und-today/2025/06/integral-integers-why-prime-numbers-fascinate-mathematicians/#:~:text=The%20search%20for%20large%20primes%20Their%20work,equals%20170%2C141%2C183%2C460%2C469%2C231%2C731%2C687%2C303%2C715%2C884%2C105%2C727%2C%20and%20that%20value%20is%20prime.)
