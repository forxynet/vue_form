<template>
<div>
    <Error :message="errorMessage" />
    <payment-view />
</div>
</template>

<script>
import PaymentView from '@/views/PaymentView';
import Error from "@/components/error";
import state from "@/state";

export default {
    components: {
        PaymentView,
        Error
    },
    setup() { 
        return {
           errorMessage: state.errorMessage
        }
    }
}
</script>
