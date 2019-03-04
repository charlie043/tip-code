const _createLabels = (data, label) => {
  if (typeof data === 'string') {
    return label
  }
  return Object.keys(data).map(key => {
    const _label = label ? `${label}.${key}` : `${key}`
    return _createLabels(data[key], _label)
  })
}

const createMessageLabels = data => {
  return flattenDeep(_createLabels(data))
}
