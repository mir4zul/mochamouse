<script setup>
import { computed } from "vue";

const emit = defineEmits(["click"]);

const props = defineProps({
  label: {
    type: String,
    default: "Button",
  },
  variant: {
    type: String,
    default: "primary",
  },
  size: {
    type: String,
    default: "md",
  },
  to: {
    type: String,
    default: null,
  },
  type: {
    type: String,
    default: "button",
  },
  disabled: {
    type: Boolean,
    default: false,
  },
  extraClass: {
    type: String,
    default: "",
  },
});

const baseClass =
    "inline-flex items-center justify-center font-extrabold uppercase rounded-full transition-all duration-200 focus:outline-none focus-visible:ring-2 focus-visible:ring-ring disabled:opacity-50 disabled:pointer-events-none";

const variants = {
  primary: "bg-primary text-white hover:bg-primary/90 active:scale-95",
  secondary: "bg-secondary text-secondary-foreground hover:bg-secondary/80",
  outline: "border border-border text-foreground hover:bg-accent",
  ghost: "text-foreground hover:bg-muted",
};

const sizes = {
  sm: "text-xs px-12 py-2",
  md: "text-xs px-10 py-2",
  lg: "text-sm px-14 py-3",
};

const classes = computed(
    () =>
        `${baseClass} ${variants[props.variant]} ${sizes[props.size]} ${props.extraClass}`
);

function handleClick(event) {
  if (props.disabled) return;
  emit("click", event);
}
</script>

<template>
  <!-- Link -->
  <a
      v-if="to"
      :href="to"
      :class="classes"
      @click="handleClick"
  >
    {{ label }}
  </a>

  <!-- Button -->
  <button
      v-else
      :type="type"
      :disabled="disabled"
      :class="classes"
      @click="handleClick"
  >
    {{ label }}
  </button>
</template>
