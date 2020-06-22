publish-us-east-1:
	sam package --s3-bucket ${bucket} --output-template-file packaged-template-use1.yml
	sam publish --template ./packaged-template-use1.yml --semantic-version 0.0.2 --region us-east-1

publish-us-east-2:
	sam package --s3-bucket ${bucket} --output-template-file packaged-template-use2.yml
	sam publish --template ./packaged-template-use2.yml --semantic-version 0.0.2 --region us-east-2
