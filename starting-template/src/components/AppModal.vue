<template>
  <div
    class="modal fade"
    id="exampleModal"
    tabindex="-1"
    aria-labelledby="exampleModalLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">
            {{ character.name }}
          </h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
          <img
            :src="character.thumbnail"
            class="img-fluid rounded-start"
            alt="..."
          />
          <div>
            <h5>Description:</h5>
            <p>
              {{ character.description }}
            </p>
            <h5>Comics:</h5>
            <ul>
              <li v-for="(el, idx) in character.comic" :key="idx">
                {{ el.name }}
              </li>
            </ul>
          </div>
        </div>
        <div class="modal-footer">
          <button
            type="button"
            class="btn btn-secondary"
            data-bs-dismiss="modal"
          >
            Close
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppModal",
  props: ["character"],
};
</script>

<style scoped></style>
