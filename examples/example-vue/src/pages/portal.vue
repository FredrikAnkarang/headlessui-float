<template>
  <div class="w-56 text-right">
      <Menu as="div" class="relative inline-block text-left" v-slot="{ open }">
          <Float floating-as="template">
              <MenuButton
                  ref="reference"
                  as="button"
                  class="inline-flex w-full justify-center rounded-md bg-black bg-opacity-20 px-4 py-2 text-sm font-medium text-white hover:bg-opacity-30 focus:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-75"
              >
                  Options
                  <ChevronDownIcon
                      class="ml-2 -mr-1 h-5 w-5 text-violet-200 hover:text-violet-100"
                      aria-hidden="true"
                  />
              </MenuButton>

              <MenuItems
                  class="box-border overflow-auto min-h-[50px] divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none">
                  <div class="px-1 py-1">
                      <MenuItem v-slot="{ active }">
                          <button
                              :class="[
                active ? 'bg-violet-500 text-white' : 'text-gray-900',
                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
              ]"
                          >
                              <PencilIcon
                                  :active="active"
                                  class="mr-2 h-5 w-5 text-violet-400"
                                  aria-hidden="true"
                              />
                              Edit
                          </button>
                      </MenuItem>
                      <MenuItem v-slot="{ active }">
                          <button
                              :class="[
                active ? 'bg-violet-500 text-white' : 'text-gray-900',
                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
              ]"
                          >
                              <PencilIcon
                                  :active="active"
                                  class="mr-2 h-5 w-5 text-violet-400"
                                  aria-hidden="true"
                              />
                              Duplicate
                          </button>
                      </MenuItem>
                  </div>
                  <div class="px-1 py-1">
                      <MenuItem v-slot="{ active }">
                          <button
                              :class="[
                active ? 'bg-violet-500 text-white' : 'text-gray-900',
                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
              ]"
                          >
                              <PencilIcon
                                  :active="active"
                                  class="mr-2 h-5 w-5 text-violet-400"
                                  aria-hidden="true"
                              />
                              Archive
                          </button>
                      </MenuItem>
                      <MenuItem v-slot="{ active }">
                          <button
                              :class="[
                active ? 'bg-violet-500 text-white' : 'text-gray-900',
                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
              ]"
                          >
                              <PencilIcon
                                  :active="active"
                                  class="mr-2 h-5 w-5 text-violet-400"
                                  aria-hidden="true"
                              />
                              Move
                          </button>
                      </MenuItem>
                  </div>

                  <div class="px-1 py-1">
                      <MenuItem v-slot="{ active }">
                          <button
                              :class="[
                active ? 'bg-violet-500 text-white' : 'text-gray-900',
                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
              ]"
                          >
                              <PencilIcon
                                  :active="active"
                                  class="mr-2 h-5 w-5 text-violet-400"
                                  aria-hidden="true"
                              />
                              Delete
                          </button>
                      </MenuItem>
                  </div>
              </MenuItems>
          </Float>
      </Menu>
  </div>
</template>

<script>
export default {
  name: 'UiDropdown'
}
</script>

<script setup>

import {ref} from 'vue';
import { Menu, MenuButton, MenuItems, MenuItem } from '@headlessui/vue'
import { Float } from '@headlessui-float/vue'

const props = defineProps({})

const emit = defineEmits([])



</script>

<style scoped>

</style>
