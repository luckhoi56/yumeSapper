<script>
    export let m_category = 'pho tai nam';
    
</script>
<style>
.dib {
    display: inline-block;
}

.b {
    font-weight: bold;
}

.link {
    text-decoration: none;
    transition: color .15s ease-in;
}

.link:link, .link:visited {
    transition: color .15s ease-in;
}

.link:hover {
    transition: color .15s ease-in;
}

.link:active {
    transition: color .15s ease-in;
}

.link:focus {
    transition: color .15s ease-in;
    outline: 1px dotted currentColor;
}

.black {
    color: #000;
}

.gray {
    color: #777;
}

.pa3 {
    padding: 1rem;
}

.mr3 {
    margin-right: 1rem;
}

.f6 {
    font-size: .875rem;
}

.dim {
    opacity: 1;
    transition: opacity .15s ease-in;
}

.dim:hover, .dim:focus {
    opacity: .5;
    transition: opacity .15s ease-in;
}

.dim:active {
    opacity: .8;
    transition: opacity .15s ease-out;
}

@media screen and (min-width: 30em) {
    .pa4-ns {
        padding: 2rem;
    }

    .f5-ns {
        font-size: 1rem;
    }
}
</style>

  <a class="buttonnav link dim gray b f6 f5-ns dib mr3" href="#" title="{m_category}">{m_category}</a>
  <!-- <a class="link dim gray    f6 f5-ns dib mr3" href="#" title="Rice">Rice</a>
  <a class="link dim gray    f6 f5-ns dib mr3" href="#" title="Vermecelli">Vermecelli</a>
  <a class="link dim gray    f6 f5-ns dib mr3" href="#" title="Store">Banhmi</a>
  <a class="link dim gray    f6 f5-ns dib mr3" href="#" title="Home">Rolls</a>
  <a class="link dim gray    f6 f5-ns dib mr3" href="#" title="About">Smoothie</a>
  <a class="link dim gray    f6 f5-ns dib mr3" href="#" title="Store">Tea</a>
  <a class="link dim gray    f6 f5-ns dib" href="#" title="Contact">Coffee</a> -->



