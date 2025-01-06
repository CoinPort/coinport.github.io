---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
## CoinPort Exchange - News Blog

News updates and articles of interest for the CoinPort Exchange members. 

<script>
  const queryString = window.location.search;
  const urlParams = new URLSearchParams(queryString);
  const theme = urlParams.get('theme');
  const className = theme=='dark-mode'?'dark-mode':'light-mode';
  document.body.classList.toggle(className);
</script>