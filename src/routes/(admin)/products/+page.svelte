<script>
  let name = "";

  let product = {
    name: "",
    overview: "",
    details: "",
  };
  const handlechange = (e, value, field) => {
    console.log(">>> handlechange - e", e);
    console.log(">>> handlechange - e.target.value", e.target.value);
    console.log(">>> handlechange - e.target.id", e.target.id);
    console.log(">>> handlechange - product", product);
    console.log(">>> handlechange - product.name", product.name);

    fieldsVerify();
  };

  const fieldsVerify = () => {
    let result = true;
    const _name = document.getElementById("name");
    const _details = document.getElementById("details");

    document.getElementById("nameMessageError").style.display = "none";
    document.getElementById("detailsMessageError").style.display = "none";

    if (!(_name.value && _name.value !== "" && _name.value.length > 3)) {
      document.getElementById("nameMessageError").style.display = "block";
      result = false;
    }

    if (
      !(_details.value && _details.value !== "" && _details.value.length > 3)
    ) {
      document.getElementById("detailsMessageError").style.display = "block";
      result = false;
    }
  };
</script>

<div class="row">
  <div class="col-md-9">
    <div class="card mt-5 mb-5">
      <div class="card-header">
        <h5 class="card-title">Card title</h5>
      </div>
      <div class="card-body">
        <div
          class="alert alert-danger"
          role="alert"
          id="alertErrorMessage"
          style="display:none"
        >
          <h4 class="alert-heading">DConfirma a deleção do registro?</h4>
          <p>nome do usuário e/ou senha incorretos</p>
          <hr />
          <p class="mb-0">Por gentileza, confira os dados digitados</p>
        </div>

        <div
          class="alert alert-danger"
          role="alert"
          id="alertErrorMessage"
          style="display:none"
        >
          <h4 class="alert-heading">Dados incorretos!</h4>
          <p>nome do usuário e/ou senha incorretos</p>
          <hr />
          <p class="mb-0">Por gentileza, confira os dados digitados</p>
        </div>

        <div
          class="alert alert-success"
          role="alert"
          id="alertSuccessMessage"
          style="display:none"
        >
          <h4 class="alert-heading">Acesso liberado!</h4>
          <p>vai ser ótimo ter você de volta</p>
          <hr />
          <p class="mb-0">redirecionando...</p>
        </div>

        <form class="row">
          <div class="mb-3 col-md-6">
            <label for="name" class="form-label">produto do produto</label>
            <input
              bind:value={product.name}
              type="text"
              id="name"
              on:change={(e) => handlechange(e)}
              class="form-control"
            />
            <span
              id="nameMessageError"
              class="form-text text-danger"
              style="display: none"
              >*** [nome do produto] - preenchimento incorreto!!!</span
            >
          </div>

          <div class="mb-3 col-md-6">
            <label for="details" class="form-label">detalhes do produto</label>
            <input
              bind:value={product.details}
              type="text"
              id="details"
              on:change={(e) => handlechange(e)}
              class="form-control"
            />
            <span
              id="detailsMessageError"
              class="form-text text-danger"
              style="display: none"
              >*** [details do produto] - preenchimento incorreto!!!</span
            >
          </div>

          <div class="mb-3 col-md-6">
            <label for="details" class="form-label">detalhes do produto</label>
            <input
              bind:value={product.details}
              type="text"
              id="details"
              on:change={(e) => handlechange(e)}
              class="form-control"
            />
            <span
              id="detailsMessageError"
              class="form-text text-danger"
              style="display: none"
              >*** [details do produto] - preenchimento incorreto!!!</span
            >
          </div>

          <div class="mb-3 col-md-6">
            <label for="exampleInputEmail1" class="form-label"
              >Email address</label
            >
            <input
              type="email"
              class="form-control"
              id="exampleInputEmail1"
              aria-describedby="emailHelp"
            />
            <div id="emailHelp" class="form-text">
              We'll never share your email with anyone else.
            </div>
          </div>

          <div class="mb-3 form-check">
            <input
              type="checkbox"
              class="form-check-input"
              id="exampleCheck1"
            />
            <label class="form-check-label" for="exampleCheck1"
              >Check me out</label
            >
          </div>
          <button type="submit" class="btn btn-primary">Submit</button>
        </form>
      </div>
      <div class="card-footer">
        powered by <a href="https://logicinfo.com.br">logicinfo</a>
      </div>
    </div>
  </div>

  <div class="col-md-3">
    <div class="card mt-5 mb-5">
      <div class="card-header">imagem</div>
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">
          Some quick example text to build on the card title and make up the
          bulk of the card's content.
        </p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
      </div>
      <div class="card-footer">
        powered by <a href="https://logicinfo.com.br">logicinfo</a>
      </div>
    </div>
  </div>
</div>
