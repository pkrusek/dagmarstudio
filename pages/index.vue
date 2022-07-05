<script setup>

const navigation = [
  {name: 'Caricatures', href: '#', current: true},
  {name: 'Art Lessons', href: '#', current: false},
  {name: 'Projects', href: '#', current: false},
  {name: 'Contact', href: '#', current: false},
]
</script>

<template>
  <div>

    <header
        class="
            fixed
            w-full
            bg-gray-200
            flex
            justify-between
            items-center
            px-4
            md:px-12
            transition-all
            duration-200
            h-24
            shadow-xl
         "
    >
      <nav>
        <ul
            class="
                  fixed
                  left-0
                  right-0
                  min-h-screen
                  px-4
                  pt-8
                  space-y-4
                  text-black
                  transform
                  transition
                  duration-300
                  translate-x-full
                  md:relative md:flex md:space-x-10 md:min-h-0 md:px-0 md:py-0 md:space-y-0 md:translate-x-0
               "
        >
          <li v-for="item in navigation" :key="item.name"><a :href="item.href">{{ item.name }}</a></li>
        </ul>
      </nav>

    </header>

  </div>
</template>

<!--<a v-for="item in navigation" :key="item.name" :href="item.href" :class="[item.current ? 'bg-gray-900 text-white' : 'text-gray-300 hover:bg-gray-700 hover:text-white', 'px-3 py-2 rounded-md text-sm font-medium']" :aria-current="item.current ? 'page' : undefined">{{ item.name }}</a>-->