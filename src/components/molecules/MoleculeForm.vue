<script setup lang="ts">
import { ValidationRule } from 'quasar';
import AtomInput from '../atoms/AtomInput.vue';
import AtomButton from '../atoms/AtomButton.vue';

interface IFormData {
  label: string,
  type: string,
  value: string | number,
  hint?: string,
  rules?: ValidationRule[]
}

interface IProps {
  onSubmit: any,
  onReset: any,
  data: IFormData[]
}

defineProps<IProps>();
</script>

  <template>
        <q-form
          @submit="onSubmit"
          @reset="onReset"
          class="q-gutter-md"
        >
        <atom-input
        v-for="item in data" :key="item.label"
        :value="item.value"
        :hint="item.hint"
        :label="item.label"
        :rules="item.rules"
        :type="item.type"
        />

          <!-- <q-toggle v-model="accept" label="I accept the license and terms" /> -->

          <div>
            <atom-button icon="success" label="Submit" type="submit" color="primary"/>
            <atom-button icon="menu" label="Reset" type="reset" color="primary" class="q-ml-sm"/>
          </div>
        </q-form>

  </template>
