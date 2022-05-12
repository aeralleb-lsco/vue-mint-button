<template>
    <div id="app">
        <MintButton :ABI="abi" :price="price" :network="network" :method="method" :contract="contract" />
    </div>
</template>

<script>
import MintButton from "./MintButton.vue";
// import MintButton from "vue-mint-button";

export default {
    name: "App",
    components: {
        MintButton,
    },
    data() {
        return {
            abi: [
                {
                    inputs: [
                        {
                            internalType: "uint256",
                            name: "number",
                            type: "uint256",
                        },
                        {
                            internalType: "bool",
                            name: "isTest",
                            type: "bool",
                        },
                    ],
                    name: "safeMint",
                    outputs: [],
                    stateMutability: "payable",
                    type: "function",
                    payable: true,
                },
            ],
            price: 0.1,
            infuraId: "be5483cf977b4d6eb4e04d0daaf10b20",
            contract: "0x2A8555f5cd838356295637b336C90368EA1ED995",
            network: "rinkeby",
            method: "safeMint",
        };
    },
};
</script>
