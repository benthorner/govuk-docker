GOVUK_DOCKER_RUN=govuk-docker run publishing-api-default

default:
	${GOVUK_DOCKER_RUN} bundle
	${GOVUK_DOCKER_RUN} sh -c 'rake db:migrate 2>/dev/null || rake db:setup'
	${GOVUK_DOCKER_RUN} rails runner 'User.first || User.create'
	${GOVUK_DOCKER_RUN} rake setup_exchange
