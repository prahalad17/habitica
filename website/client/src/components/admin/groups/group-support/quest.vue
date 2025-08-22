<template>
  <div>
    <form-row
      v-model="group.quest.key"
      label="Quest Identifier"
      :editable="false"
    />
    <form-row
      v-model="group.quest.leader"
      label="Quest Leader"
      :editable="false"
    >
      <template slot="subtitle">
        <router-link
          :to="{'name': 'adminPanelUser', 'params': {'userIdentifier': group.quest.leader}}"
        >
          {{ group.quest.leader }}
        </router-link>
      </template>
    </form-row>
    <form-row
      v-model="group.quest.active"
      label="Is Quest Active"
      input-type="checkbox"
    />
  </div>
</template>

<script>
import formRow from '@/components/admin/formRow.vue';

export default {
  components: {
    formRow,
  },
  props: {
    group: {
      type: Object,
      required: true,
    },
  },
};
</script>
