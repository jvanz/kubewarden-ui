<script>
import { _CREATE } from '@shell/config/query-params';

import { KUBEWARDEN } from '@kubewarden/types';

import PolicyDetail from '@kubewarden/components/Policies/PolicyDetail';

export default {
  name: 'ClusterAdmissionPolicy',

  props: {
    mode: {
      type:    String,
      default: _CREATE,
    },
    value: {
      type:     Object,
      required: true,
    },
  },

  components: { PolicyDetail },

  data() {
    return { resource: KUBEWARDEN.ADMISSION_POLICY };
  }
};
</script>

<template>
  <PolicyDetail :value="value" :mode="mode" :resource="resource" />
</template>
