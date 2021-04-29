# Заметки о Mathjax

1. To see how any of the formulas were made in any question or answer,
   including this one, use the "edit" link to view the complete source. To
   quickly see the source of a single expression, right-click on it and choose
   "Show Math As > TeX Commands".

  (Note that in some browsers, such as Firefox, the MathJax right-click menu
  that contains this command will be obscured by the browser's own right-click
  menu. Click somewhere outside the main browser canvas -- such as in the
  address bar -- to dismiss the browser menu and reveal the MathJax one behind
  it).

2. For inline formulas, enclose the formula in \\$...\\$. For displayed
   formulas, use \\$\\$...\\$\\$. These render differently. For example, type
   `$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$` to show $\sum_{i=0}^n i^2
   = \frac{(n^2+n)(2n+1)}{6}$ (which is inline mode) or type 
   ```$$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$``` 
   to show $$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$$ 
   (which is display mode).

3. For Greek letters, use `\alpha, \beta, ..., \omega`: $\alpha, \beta, ...,
   \omega$. For uppercase, use `\Gamma, \Delta, ..., \Omega`: $\Gamma, \Delta,
   ..., \Omega$. Some Greek letters have variant forms: `\epsilon \varepsilon`
   ϵ, ε, `\phi \varphi` ϕ, φ, and others.

4. For superscripts and subscripts, use `^` and `\_`. For example, `x_i^2`:
   $x_i^2$, `log_2 x`: $log_2 x$.

5. **Groups**. Superscripts, subscripts, and other operations apply only to
   the next “group”. A “group” is either a single symbol, or any formula
   surrounded by curly braces `{...}`. If you do `10^10`, you will get
   a surprise: $10^10$. But `10^{10}` gives what you probably wanted:
   $10^{10}$. Use curly braces to delimit a formula to which a superscript or
   subscript applies: `x^5^6` is an error; `{x^y}^z` is ${x^y}^z$, and
   `x^{y^z}` is $x^{y^z}$. Observe the difference between `x_i^2` $x_i^2$ and
   `x_{i^2}` $x_{i^2}$.

6. Parentheses Ordinary symbols `()[]` make parentheses and brackets (2+3)[4+4].
   Use \{ and \} for curly braces {}.

  These do not scale with the formula in between, so if you write
  `(\frac{\sqrt x}{y^3})` the parentheses will be too small: 
  $(\frac{\sqrt x}{y^3})$. Using `\left(...\right)` will make the sizes adjust
  automatically to the formula they enclose: 
  `\left(\frac{\sqrt x}{y^3}\right)` is $\left(\frac{\sqrt x}{y^3}\right)$.

  `\left` and `\right` apply to all the following sorts of parentheses: `(`
  and `)` $(x)$, `[` and `]` $[x]$, \{ and \} ${x}$, `|` |x|, `\vert` |x|,
  `\Vert` ∥x∥, `\langle` and `\rangle `⟨x⟩, `\lceil` and `\rceil` ⌈x⌉, and
  `\lfloor` and `\rfloor` ⌊x⌋. `\middle` can be used to add additional
  dividers. There are also invisible parentheses, denoted by `.`:
  `\left.\frac12\right\rbrace` is $\left.\frac12\right\rbrace$.

  If manual size adjustments are required:
  `\Biggl(\biggl(\Bigl(\bigl((x)\bigr)\Bigr)\biggr)\Biggr)` gives
  $\Biggl(\biggl(\Bigl(\bigl((x)\bigr)\Bigr)\biggr)\Biggr)$.


-------

My notes:

Punctuation marks should be out of math expression.
