<script>
  import Footer from "../../lib/components/layout/footer.svelte";
  import Header from "../../lib/components/layout/header.svelte";
  import Sidebar from "../../lib/components/layout/sidebar.svelte";
</script>

<div class="container-fluidx">


  <div class="container">
    <div class="row">
      <div class="col-md-3">
        <Sidebar />
      </div>
      <div class="col-md-9">
        <Header />
        <slot />
      </div>
    </div>
  </div>

  <Footer />
</div>
