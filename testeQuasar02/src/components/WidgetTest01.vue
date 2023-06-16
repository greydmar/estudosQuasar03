<template>
    <div class="q-pa-md row items-start q-gutter-md">
      <q-card class="my-card" flat bordered>
        <q-card-section>
          <div class="row items-center no-wrap">
          <div class="col">
            <div class="text-h6">{{titulo}}</div>
          </div>
          <div class="col-auto">
            <q-btn color="grey-7" round flat icon="more_vert">
              <q-menu cover auto-close>
                <q-list>
                  <q-item clickable>
                    <q-item-section>Expandir</q-item-section>
                  </q-item>
                  <q-item clickable>
                    <q-item-section>Esconder</q-item-section>
                  </q-item>
                </q-list>
              </q-menu>
            </q-btn>
          </div>
        </div>
        </q-card-section>
        <q-img
          src="https://cdn.quasar.dev/img/parallax2.jpg"
        />
        <q-card-section>
          <div class="text-overline text-orange-9">Overline</div>
          <div class="text-h5 q-mt-sm q-mb-xs">Title</div>
          <div class="text-caption text-grey">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </div>
        </q-card-section>
        <q-card-actions>
          <q-btn flat color="primary" label="Share" />
          <q-btn flat color="secondary" label="Book" />
          <q-space />
          <q-btn
            color="grey"
            round
            flat
            dense
            :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
            @click="expanded = !expanded"
          />
        </q-card-actions>
        <q-slide-transition>
          <div v-show="expanded">
            <q-separator />
            <q-card-section class="text-subitle2">
              {{ lorem }}
            </q-card-section>
          </div>
        </q-slide-transition>
      </q-card>
    </div>
  </template>
<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      titulo: 'Pasta 01',
      expanded: ref(false),
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
    }
  }
}
</script>
<!-- <style lang="sass" scoped>
   .my-card
      width: 100%
      max-width: 350px
</style> -->
