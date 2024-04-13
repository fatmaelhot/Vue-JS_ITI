<template>
  <nav class="navbar navbar-expand-lg bg-dark my-5">
    <div class="container-fluid">
      <a class="bookStore text-decoration-none text-warning "  @click.prevent="$emit('toggleWishlist')"
        >Book Store</a
      >
      <p class="m-auto p-2 ">Book in wish list {{counter}}</p>
      <button
        class="navbar-toggler "
        type="button"
        data-toggle="collapse"
        data-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <a class="btn btn-danger" aria-current="page" type="button" @click.prevent="$emit('toggleWishlist')">WishList</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  props: ['wishlist', 'isWishlistVisible'],
  emits: ['toggleWishlist']
};
</script>
