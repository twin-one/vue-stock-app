<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-5">
                <!-- <div class="quote" v-if="stock.symbol"> -->
                <div class="quote">
                    <div class="row">
                        <div class="col-6">Symbol:</div>
                        <div class="col-6">{{stock.Symbol}}</div>
                    </div>
                    <div class="row">
                        <div class="col-6">Company Name:</div>
                        <div class="col-6">{{stock.Name}}</div>
                    </div>
                    <div class="row">
                        <div class="col-6">Latest Price (USD):</div>
                        <div class="col-6">{{stock.latestPrice}}</div>
                    </div>
                    <div class="row">
                        <div class="col-6">Change (USD):</div>
                        <div class="col-6">{{stock.change}}</div>
                    </div>
                    <div class="row">
                        <div class="col-6">Change (%):</div>
                        <div class="col-6">{{stock.changePercent}}</div>
                    </div>
                    <div class="row">
                        <div class="col-6">Latest Time:</div>
                        <div class="col-6">{{stock.latestTime}}</div>
                    </div>
                </div>
            </div>
            <div class="col-7">
                <div class="graph row" id="graph"></div>
            </div>
        </div>
    </div>
</template>

<script>
module.exports = {
  props: ["stock"]
};
</script>

<style>
.quote {
  margin-top: 50px;
}

.quote .row {
  padding: 10px;
}

.quote .row div:first-child {
  font-weight: 500;
}

.quote .row:nth-child(odd) {
  background-color: #f0f0f0;
}
</style>