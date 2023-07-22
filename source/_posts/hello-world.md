---
title: Hello World
date: 2023/07/20
math: true
categories:
- Mathematics for Computer Graphics
tags:
- Math
---


Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Math test

This is inline latex: $c = \pm\sqrt{a^2+b^2}$

This is block level latex:

$$
c = \pm\sqrt{a^2+b^2}
$$

This is block level latex with new lines:
$$
\begin{array}{}
\hat{f}\left( \xi \right) =\int_{-\infty}^{\infty}{f\left( x \right) e^{-2\pi ix\xi}\mathrm{d}x}
\\\\
e^{i\varphi}=\cos \varphi +i\sin \varphi 
\\\\
e^{i\pi}+1=0
\end{array} 
$$


$$
\boldsymbol{A}=\left[ \begin{array}{l}
	a_{11}&		a_{12}&		\cdots&		a_{1n}\\\\
	a_{21}&		a_{22}&		\cdots&		a_{2n}\\\\
	\vdots&		\vdots&		\ddots&		\vdots\\\\
	a_{n1}&		a_{n2}&		\cdots&		a_{nn}\\\\
\end{array} \right] 
$$

$$
\boldsymbol{Ax}=\left[ \begin{array}{l}
	a_{11}&		a_{12}&		\cdots&		a_{1n}\\\\
	a_{21}&		a_{22}&		\cdots&		a_{2n}\\\\
	\vdots&		\vdots&		\ddots&		\vdots\\\\
	a_{m1}&		a_{m2}&		\cdots&		a_{mn}\\\\
\end{array} \right] \left[ \begin{array}{l}
	x_1\\\\
	x_2\\\\
	\vdots\\\\
	x_n\\\\
\end{array} \right] =\left[ \begin{array}{c}
	a_{11}x_1+a_{12}x_2+\cdots +a_{1n}x_n\\\\
	a_{21}x_1+a_{22}x_2+\cdots +a_{2n}x_n\\\\
	\vdots\\\\
	a_{m1}x_1+a_{m2}x_2+\cdots +a_{mn}x_n\\\\
\end{array} \right] \in \mathbb{R} ^m
$$



### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)
