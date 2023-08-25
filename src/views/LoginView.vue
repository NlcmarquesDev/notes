<template>
  <main>
    <div class="d-flex top" >
        <a class="navbar-brand logo mx-auto" href="/">NOTES</a>
      </div>
    <div class="box d-flex justify-content-center align-items-center">
      <section>
        <div class="mx-auto form shadow p-3 mb-5 bg-white rounded ">
          <h3 class="text-center " >Login</h3>
          <hr>
          <p class="fw-bold m-0">Demo Account</p>
          <div class="d-flex gap-2">
            <p><span class="fw-bold">Email:</span> test@test.com</p>
            <p><span class="fw-bold">Pass:</span> test123</p>
          </div>
          <hr>
          <form class="d-flex flex-column gap-3" action="">
            <input class="form-control" type="text" name="email" id="email" placeholder="email">
            <input class="form-control"  type="password" name="password" id="password" placeholder="password">
            <button class="btn btn-primary" type="submit">Login</button>
          </form>
          <hr>
          <p class="fw-semibold">Dont't have account? 
            <a class="text-decoration-none " href="/register">Register</a>
          </p>
        </div>
      </section>
     
      
        
      
      
    </div>
  </main>
</template>

<style lang="scss" scoped>
h3{
  font-weight: 800;
}
.top{
  background-color: #f2f5fa;
}

.box {
  width: 100%;
  height: calc(100vh - 34px);
  background-color: #f2f5fa;
}
</style>
