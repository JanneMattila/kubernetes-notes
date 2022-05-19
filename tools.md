# Tools

Here are some CLI tools that can help you built your automations:

## curl

[curl](https://github.com/curl/curl)

> Curl is a command-line tool for transferring data specified with URL syntax

See usage example [here](https://github.com/JanneMattila/hassio-addon-azuredns/blob/main/addon/run.sh).

## jq

[jq](https://github.com/stedolan/jq)

> jq is a lightweight and flexible command-line JSON processor

See usage example [here](https://github.com/JanneMattila/yarp-aad-le/blob/main/deploy.sh).

## yq

[yq](https://github.com/mikefarah/yq)

> yq a lightweight and portable command-line YAML, JSON and XML processor

Example install command:

```bash
VERSION=v4.25.1
BINARY=yq_linux_amd64
sudo wget https://github.com/mikefarah/yq/releases/download/${VERSION}/${BINARY} -O /usr/bin/yq && sudo chmod +x /usr/bin/yq
```

Example usage:

```bash
# Example file
> cat configmap.yaml
apiVersion: v1
data:
  myname: myvalue
  myname2: myvalue2
kind: ConfigMap
metadata:
  creationTimestamp: null
  name: myconfig

# Get single property value
> cat configmap.yaml | yq "(.data.myname)"
myvalue

# Update property value
> cat configmap.yaml | yq "(.data.myname)|=\"hello\""
apiVersion: v1
data:
  myname: hello
  myname2: myvalue2
kind: ConfigMap
metadata:
  creationTimestamp: null
  name: myconfig

# Deploy using updated property values
> cat configmap.yaml | \
    yq "(.data.myname)|=\"hello\"" | \
    yq "(.data.myname2)|=\"world\"" | \
  kubectl apply -f -

# Deploy using updated property values for variables
> myvar1="hello"
> myvar2="world"
> cat configmap.yaml | \
    yq "(.data.myname)|=\"$myvar1\"" | \
    yq "(.data.myname2)|=\"$myvar2\"" | \
  kubectl apply -f -
```
