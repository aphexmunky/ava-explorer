<template>
    <div class="top_info">
        <top-assets></top-assets>
        <meta-data></meta-data>
        <transaction-history></transaction-history>
    </div>
</template>
<script>
import TopAssets from "@/components/Home/TopInfo/TopAssets";
import MetaData from "@/components/Home/TopInfo/MetaData";
import TransactionHistory from "./TransactionHistory";

export default {
    components: {
        TopAssets,
        MetaData,
        TransactionHistory
    }
};
</script>

<style scoped lang="scss">
@use '../../../main';

.top_info {
    display: grid;
    grid-template-columns: minmax(0, 30%) 1fr 360px;
    padding: 25px 0px;
    overflow: auto;

    > div {
        padding: 0px 35px;
        overflow: auto;
        border-right: 1px solid #c4c4c455;
    }

    > div:last-of-type {
        border: none;
    }
}

h4 {
    margin: 0;
    margin-bottom: 20px;
    font-size: 12px;
}

@media only screen and (max-width: main.$mobile_width) {
    .top_info {
        grid-template-columns: 1fr;
        grid-template-rows: max-content max-content max-content;

        > div {
            padding: 14px;
            border: none;
            border-bottom: 1px solid #c4c4c455;
        }
    }
}
</style>
