project_name = 'citus-manager'
image_ref = 'k3d-registry.localhost:5001/' + project_name

docker_build(
    image_ref,
    context='.',
    dockerfile='./Dockerfile',
    live_update=[
        sync('./manager/', '/app'),
    ]
)
k8s_yaml('./test-rig/manager-deployment.yaml')
