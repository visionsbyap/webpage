<template>
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { Image } from "~/../types/image";
interface Props {
  title: string;
  description?: string;
  includedFeatures: string[];
  price: string;
  currency?: string;
  image?: Image;
}

withDefaults(defineProps<Props>(), {
  description: "",
  currency: "",
});
</script>
