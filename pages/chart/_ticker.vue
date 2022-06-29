<template>
  <div>
		<!-- TradingView Widget BEGIN -->
		<div class="tradingview-widget-container">
			<div id="tradingview_3b098"></div>
			<script type="text/javascript">
			
			</script>
		</div>
		<!-- TradingView Widget END -->
	</div>
</template>

<script>
export default {
	mounted() {
		const ticker = this.$route.params.ticker.toUpperCase();
		const assetType = this.$route.query.type;
		let exchange = this.$route.query.exchange;
		
		if (typeof(exchange) === "undefined") {
			exchange = "BINANCE"
		} else {
			exchange = exchange.toUpperCase()
		};

		new TradingView.MediumWidget({
			"symbols": [
				[
					ticker,
					`${exchange}:${ticker}${assetType == "crypto" ? 'USD':''}|12M`
				],
				[
					assetType === "crypto" ? "Bitcoin":"HXT",
					assetType === "crypto" ? "BINANCE:BTCUSD|12M":"HXT|12M"
				]
			],
			"chartOnly": false,
			"width": "800",
			"height": "400",
			"locale": "en",
			"colorTheme": "dark",
			"gridLineColor": "rgba(42 ,46, 57, 0)",
			"fontColor": "#787B86",
			"isTransparent": false,
			"autosize": true,
			"showFloatingTooltip": true,
			"showVolume": false,
			"scalePosition": "no",
			"scaleMode": "Normal",
			"fontFamily": "Trebuchet MS, sans-serif",
			"noTimeScale": false,
			"chartType": "area",
			"lineColor": "#2962FF",
			"bottomColor": "rgba(41, 98, 255, 0)",
			"topColor": "rgba(41, 98, 255, 0.3)",
			"container_id": "tradingview_3b098"
		});
	},
}
</script>
