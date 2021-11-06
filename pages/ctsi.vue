<template>
  <div>
		<!-- TradingView Widget BEGIN -->
		<div class="tradingview-widget-container">
			<div class="tradingview-widget-container__widget"></div>
			<script type="text/javascript" src="https://s3.tradingview.com/external-embedding/embed-widget-single-quote.js" async>
			{
				"symbol": "BINANCE:CTSIUSDT",
				"width": 350,
				"colorTheme": "dark",
				"isTransparent": false,
				"locale": "en"
			}
			</script>
		</div>
		<!-- TradingView Widget END -->
	</div>
</template>

<script>
export default {}
</script>
