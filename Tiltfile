custom_build(
    ref='library/config-service',
    command='gradlew bootBuildImage --imageName %EXPECTED_REF%',
    deps=['build.gradle', 'src']
)

k8s_yaml(['k8s/app/config-service.yml'])

k8s_resource('config-service', port_forwards=['8888'])
