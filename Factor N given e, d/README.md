
$\Huge\text{The problem: given d and e, can we factorize N ?}$

-------

Ta có: $de \equiv 1 (mod$ $\phi(N))$. 
Gọi $k = de - 1 = t * \phi(N)$, $k$ chẵn.
$\rightarrow k = 2^i * r$, với $r$ lẻ, $i \ge 1$.

Để phân tích $p, q$ thì ta sẽ làm như sau: 
Dựa trên bài toán tìm nghiệm $x$ thỏa mãn $x^2 \equiv 1 (mod$ $N)$.

Chọn $1$ số ngẫu nhiên $g$ sao cho $gcd(g, N) = 1$.
$\rightarrow$ $g^{\phi(N)} \equiv 1 (mod$ $N)$ theo định lí Euler.
$\rightarrow$ $g^k \equiv 1 (mod$ $N)$ vì $k$ là bội của $\phi(N)$.

Gọi $t$ $=$ $g^{\frac{k}{2}}$, ta có phương trình $t^2 \equiv 1 (mod$ $N)$. 
Dùng CRT để giải phương trình này ta có 4 nghiệm: $t = 1, t = -1, t = a, t = -a$.

- Với $t = 1$, ta đặt $h$ $=$ $g^{\frac{k}{4}}$ rồi giải tiếp phương trình $h^2 = t =$ $g^{\frac{k}{2}}$ $\equiv 1 (mod$ $N)$
- Với $t = -1$, do $1 < t < N$ và $t + 1 = s * N = s *pq$. Suy ra $s = 1$ từ đó ta có $t = pq - 1$. Đến đây ta không thể phân tích $p, q$ được nữa nên ta sẽ random số $g$ khác.
- Với $t = a$ $(mod$ $pq)$ và $1 < a < pq$ và $a$ thỏa mãn:
$$
\begin{cases}
a \equiv 1 \mod p \\
a \equiv -1 \mod q 
\end{cases}
$$
Từ đó ta có thể lấy $gcd(a - 1, pq)$ là sẽ ra được $p$.

- Tương tự với $t = -a$, ta lấy $gcd(a - 1, pq)$ là sẽ ra $q$.



-----

