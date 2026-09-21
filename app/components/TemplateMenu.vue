<template>
  <UDropdownMenu
    v-slot="{ open }"
    :modal="false"
    :items="[{
      label: 'Zaeth',
      to: 'https://sai.st'
    }, {
      label: 'Sai',
      to: 'https://zaeth.com',
      color: 'primary',
      checked: true,
      type: 'checkbox'
    }, {
      label: 'Next',
      to: 'https://next.yt'
    }]"
    :content="{ align: 'start' }"
    :ui="{ content: 'min-w-fit' }"
    size="xs"
  >
    <UButton
      label="Zaeth"
      variant="subtle"
      trailing-icon="i-lucide-chevron-down"
      size="xs"
      class="-mb-[6px] truncate rounded-full font-semibold"
      :class="[open && 'bg-primary/15']"
      :ui="{
        trailingIcon: ['transition-transform duration-200', open ? 'rotate-180' : undefined].filter(Boolean).join(' ')
      }"
    />
  </UDropdownMenu>
</template>
