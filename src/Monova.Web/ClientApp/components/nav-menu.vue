<template>
       <div class="nk-sidebar">
            <div class="nk-nav-scroll">
                <ul class="metismenu" id="menu">
                   <li class="nav-label" v-for="(route, index) in routes" :key="index">
                            <router-link :to="route.path" exact-active-class="active">
                                <icon :icon="route.icon" class="icon-speedometer menu-icon" /><span>{{ route.display }}</span>
                            </router-link>
                        </li>

                </ul>
            </div>
        </div>

</template>

<script>
    import { routes } from '../router/routes'

    export default {
      data () {
        return {
          routes,
          collapsed: true
        }
      },
      methods: {

      }
    }
</script>
