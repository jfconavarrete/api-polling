# api-polling
Shell scripts to do short-polling on a REST API using cURL and CRON.

The poll.sh script takes the following parameters:
* TARGET_DIR the directory where the response of the request will be stored.
* SOURCE_NAME a tag used to name the response file
* URL the url of the endpoint to poll
* FROM the recipient of the alert email
* TO the destination of the alert email
* SIZE_THRESHOLD the minimum number of bytes we expect the response to be. Retry the request if the threshold is not met
* TMP_FOLDER folder where the files that do not meet the will be stored
* HEADERS_FILE (optional) file with headers that will be included in the request

The resulting file will be named {SOURCE_NAME}+%Y-%m-%d:%H:%M:%S.json
