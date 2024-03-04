
<script>
  function clearQuery(params) {
    const urlParams = new URLSearchParams(window.location.search);
    const param1Value = urlParams.get('param1');
    const param2Value = urlParams.get('param2');

    urlParams.delete('param1');
    urlParams.delete('param2');

    const newUrl = `${window.location.pathname}?${urlParams.toString()}`;

    window.history.replaceState({}, document.title, newUrl);
  }

</script>
