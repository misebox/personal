# personal


[職務経歴書](https://misebox.github.io/personal/history.html)

氏名、会社名を伏せたい場合は、上記リンクからページを表示の上、
次のスクリプトをdevtools コンソールから実行

```
// /:(.*株式会社.*)/ というテキストを含む h3 要素を探して、: ＊＊＊＊＊＊＊＊＊＊に置換する
[...document.querySelectorAll("h3")].forEach(h3 => {h3.innerText?.includes("株式会社") && (h3.innerHTML = h3.innerText.replace(/:.+/, ": ＊＊＊＊＊＊＊＊＊＊")) && console.log(h3.innerText)});
// 氏名を伏せる
[...document.querySelectorAll("p")].forEach(p => {p.innerText?.includes("氏名：") && (p.innerHTML = p.innerText.replace(/氏名：.+/, "氏名：＊＊＊＊＊＊＊＊"))});
// このページをへのリンクをを消す
[...document.querySelectorAll("a")].forEach(a => {a.href.includes("misebox") && a.remove()});
// scriptタグを消す
[...document.querySelectorAll("script")].forEach(s => { s.remove()});

```

その後、コンテキストメニューから印刷を選び、ヘッダーとフッターをつけずにPDF出力する。

[Credly](https://www.credly.com/users/kazutaka-mise/badges)


