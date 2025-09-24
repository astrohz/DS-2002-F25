.PHONY: all fetch analyze clean

all: analyze

fetch:
	@echo "Starting fetch..."
	./fetch_metars.sh
	@echo "Fetching complete."

analyze: fetch
	@echo "Starting data analysis..."
	./analyze_data.sh
	@echo "Finished analyzing data, output in 'weather_report.csv'. The pipeline has completed."

clean:
	@echo "Starting cleanup..."
	rm -rf raw_metars weather_report.csv
	@echo "Cleanup complete."
