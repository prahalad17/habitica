<template>
  <div v-if="group.purchased.plan">
    <form-row
      v-model="group.purchased.plan.paymentMethod"
      label="Payment Method"
      :editable="false"
    />
    <form-row
      v-model="group.purchased.plan.planId"
      label="Plan ID"
      :editable="false"
    />
    <form-row
      v-model="group.purchased.plan.customerId"
      label="Customer ID"
      :editable="false"
    />
    <form-row
      v-model="group.purchased.plan.dateCreated"
      label="Creation Date"
      :editable="false"
    />
    <form-row
      v-model="group.purchased.plan.dateTerminated"
      label="Termination Date"
      :editable="false"
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
