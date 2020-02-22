<template>
  <symbol>
    <svg
      id="blackList"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="45px" height="52px">
      <image  x="0px" y="0px" width="45px" height="52px"  xlink:href="data:img/png;base64,iVBORw0KGgoAAAANSUhEUgAAAC0AAAA0CAAAAAA7qO4VAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QA/4ePzL8AAAAHdElNRQfkAhYKOg6BNd6/AAABmUlEQVRIx+2WsUsCcRTHv6d36lIiXZiQLpGDgyBBEITgEhr9CVZDCP4HQpCTILi526J/gEs4uLQ4SBK6FJS0WIv0C7HgEIl7DdfZqad5oOHQW+54v8/vy5f33j2OIxgIkxEYvPL4uC4/MsZk+2Zg/0icjBMRVcOCJmMO5SXSDxBRAhCCqXK9JfXalWzEAtjjtWFMukirNI9kR3PSze0B8GeaakJupF0wExFxBHAYLcz9ZeEV2NrZtstvjN20ASgMESnmh6NfjDoGlz2xksLoawMAPu/qL+8mURS9XpWZQg+FwhjrzjzojdPFaXMmI7TVaoS2LZK2Lc63z61Pz2NOzgsTLunOt/Nk7Iv8bb5ndjIplofm1ZeHJmNMXnUHfPwUnIiAUswzSDiixb7OTtNUEIBzVxTXTN3m7ROwfnzm062gou1KN2RVpZnxA9jLdTXKnSR4dQ8CIzu1FrcDlki20u5JrXo5FRSAxA89ZlPKh8waH0K4StM7z64q9Wdlsx2EVr7dzzgny9b5f/pvaR7AITcrzS3wb8YY/QUJ3FwEFuucWwAAAABJRU5ErkJggg==" />
    </svg>
    <svg
      id="coll"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="52px" height="50px">
      <image  x="0px" y="0px" width="52px" height="50px"  xlink:href="data:img/png;base64,iVBORw0KGgoAAAANSUhEUgAAADQAAAAyCAAAAAA2SqcqAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QA/4ePzL8AAAAHdElNRQfkAhYLBzFcedELAAACeElEQVRIx83WXUhTYRwG8GfqRp3wbEY15oIKki2lXIQg2k2GEV30gVkZhFAY0S4KuugDzC66DDHwQjOhsk+IMjL7IInoJpJwBLP50UwTJRrlWTQ3rT1dnG2d4szzrm46V895th/v+b/nsB0TkfmR9Rfmn1DgoMcqy7Is51e2xY0VSfKypGnWR2hwgCQHLfD6FEVRFGXi1jLUCqFdOPqrGZKyP4ogF4KaqhoXDVAWAExisWamMvSK7N5SDGuqtegTQUXwayqP6U1EABWiX1NZS6NPMl4J23BP4OYOwB7XbM5bOAW2nMvRqy2t+GK85diCbs3i0SikOa9OD7XEyi3GMzEyL2sitfgdMx6IzMRqNGhMvcizRz6HY0ZNj8w4QTHE1bihhjqUGJkUakWZGoYldImibwtxX01NcE4JIp6HS53qRzn2iKJZN5rUNJiLU4KIXcgLqelxDi4IIm5CVSK1I6dTEI1Y0ZaIp5HdkupDY/H0iNexYCARzwDH1a92FAF5Ozs+p0Pch+JwIl4yoypExg8BVieA7FV7G4O6KOzCxlgiP5Vhvx0/AOncNMeaKy0AsCOsgzjiQE1ygOAGwA3pmXoWe92+34Z133UQfTK8SRVvyU0ZkuSHAjTrIfZYUJO8Qo4ee/nbh3dRoYvYI6NCSXN/JpGvj+hzYE1AH01BToP43g2pNVPEcC2w/VOGiLxpg61xJkPE0c1AQWeGiHxYCJRei/2BrHMjzjYvAuz145qqDx4DREbaigFTScOr5DNyGHWGiOSL3fMBLNl68mrf13dHIAVEEDnd7V2R/Am3XFE7k8gL1ZDP3+8fzy8+u1I9F0L6fzX/LfoJI6sWPoFnlwcAAAAASUVORK5CYII=" />
    </svg>
    <svg
      id="answer"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="39px" height="48px">
      <image  x="0px" y="0px" width="39px" height="48px"  xlink:href="data:img/png;base64,iVBORw0KGgoAAAANSUhEUgAAACcAAAAwCAAAAAC3GzzKAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QA/4ePzL8AAAAHdElNRQfkAhYLCCMoWLyMAAABNklEQVQ4y+2Tv0rDUBTGv2QwOXVwcNAl3QpuRREKGkH8k1u3gq/SB8jcR6ntrqUgpA8QiP/QtUuTNl0ET3EoLokm7U1vd/tN9+P8+M4953I1xmdrEDAWtX3Uy3n2LMgVcEZaeDy03cPSIvS1i/1e5c/rreHZw+kShhIwcj4y3ACuLu97PnLef41mzqYkowjT28e9+4M0bwaSx4G6F6F4SzkUi7qXUQqu4mB2rsbiVc3B7FyPxYuag3HnTOrPag5GW0zqT2oORrse3wTQAJbW89s6KcwTOecX5mX1vZO5X4OIqCHltpbm0Ioi1+oLUu8l0X/jACQ/WUhKIqmp8rTsafMecm32LOPMNeZgmHoVvpLzUdVtuHMFNndhI7Rg92MuVty3YYVgr6zsW/YYzFGzRisgqjUj5h+aTpMJTjwPHAAAAABJRU5ErkJggg==" />
    </svg>
    <svg
      id="users"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="60px" height="50px">
      <image  x="0px" y="0px" width="60px" height="50px"  xlink:href="data:img/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAAyCAMAAAA3KEgwAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAABMlBMVEX////2+enT5Ji00U+jxieZwA6z0EyixiXI3X/3+uv5+/DF23aXvwuTvAKyz0mawRLX56Hs89GixSSUvQO10VDw9tv6/PT///7d6q6qyjfR45Pr88/V5ZuUvQTP4o6fwxy51Fv9/vr9/vnY56Pn8MW91mOvzkP9/vu91mSpyjTv9dmWvgnx997v9tr3+uzm78PL34O912XF3HjD2nGsyzvh7biszDzl78L0+OWcwhaWvgiWvgefxB2pyjXm8MSVvQWjxibR45KwzkahxSPH3Xz5/PGZwA+kxii30lXb6ary99/e67GszD3L34Tw9tycwRXr89DZ6KaVvgbG3HqmyC2z0E37/fbe67Lg7LWnyC/7/fXo8cmdwxnf67PV5Zyy0EvN4Ii10VHW5p7q8s6lxyuawBEyzr2JAAAAAWJLR0QAiAUdSAAAAAd0SU1FB+QCFgsJBnpHWYoAAAG/SURBVEjH7ZRXV8JAEIUDsoDGqxSJosYIVozBrqioICJYwd67/v+/oCcHyRCTLMe8KfOye2/225bZEYRWCILH2+ZjzNfm9RDTHwi289EOsRO16BQ76nYX0B3iseEIoj2hmCTFQj1RRMLffm9fHOh3ZgcY4nUgHAcbML4NyhhyPK6C4YQhk8NQyMFH5OioAzyG8QmqJ8YxSaSIlD07JavTjc60KmuGSjPM2MKzmDNbc5glah4LtvAilszWEpaJWnHYt4KM2cpAISqNVVt4DQmzlcAavUCs28JZq5WzTa68zD/zhi3s6rY1/n/etIVdZZie20lDmnN7yzG3Xb0qd+/ZXSUR9BqWYyz3mxrWir8dmfx2QcXPUAvb+Yb64o/seBrRomgF1icQi8bQr0Td9VI2VoJc3ttPWuwoub9XllGKGc7BIXBkyOMKUlWHI1VTqBwTfXKKs+++dI6LS8cLufTjXCL6SsV1rRvEzS3nOm9vEKT6CIFevfNV1u64P+MOLE0nu8eD3nnEE5cVhCc8Uvlcq9IveG0CfsULlW9411sftCZgDT4qi/jQWwapCVgCa9AAbXhhGvYfYf8FbXhhNewTQ3g3/+E9w6YAAAAASUVORK5CYII=" />
    </svg>
    <svg
      id="search"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="20px" height="21px">
      <image  x="0px" y="0px" width="20px" height="21px"  xlink:href="data:img/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAVCAAAAABjvpF0AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QA/4ePzL8AAAAHdElNRQfkAhYMAR/Tum3HAAAA1klEQVQY02XQoW+EMBTH8W/LVlRDcghyAsV6QZw7xf8vMJsj2WWMGcQFgSBVNCGdaI4xeKbpJ6/pez/hOdYLwNIP1imd5VFA4eHRzOESX89P/L6TFKlyYzdRvgV8fAhjBIBvW387A3JpMBcRXl0MzQLIfk7M+q1J5h6QA4VYURQMgLSkmwlTLCAdaoMKB8hwPCu0SM24wRENyIzub33fkQEyj6d2xfsU54CMrrRfodd/dpTRcXd0pfYplT9WVwrh/+XpaqsrJXbJu9rqao+42p4OiHt//QVIN1ic3+7d0gAAAABJRU5ErkJggg==" />
    </svg>
    <svg
      id="breadcrumbsHome"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="20px" height="23px">
      <image  x="0px" y="0px" width="20px" height="23px"  xlink:href="data:img/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAXCAAAAAAudjB/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QA/4ePzL8AAAAHdElNRQfkAhYMByet4nLfAAAAnUlEQVQY07WQuw2DQBBE31kmpADog5iAjAqukJNoA/ogpQOKgA4ogASBNA7gwAdOPdHO06z2Y8RTL1+MWTaeVLvaGOL2MDvcHFgLbrvglBPVUh2RTx72KWmvrwKp8YG9pZGYLbj1mKDVgZ0prqF+jQIYFGgAA/ebjF+/3H0pSWfS+PsAw5vA3h7y80t/hwldSDoSqmewYqmSECXV8gE6H4WN4hXrrgAAAABJRU5ErkJggg==" />
    </svg>
    <svg
      id="breadcrumbsArrow"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="15px" height="8px">
      <image  x="0px" y="0px" width="15px" height="8px"  xlink:href="data:img/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA8AAAAICAAAAAADuPouAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QA/4ePzL8AAAAHdElNRQfkAhYMCAZmE35OAAAAQ0lEQVQI12P4Dwd/H/3//58Bwf+t+hyVz6D9+j8Lw7NmBgj4x3DVbR8LA8NvKP8/A8M/VPWar1D4yk9RzPv74P///wAF7lvdUhvqZAAAAABJRU5ErkJggg==" />
    </svg>
  </symbol>
</template>

<script>
    export default {
        name: "svgElements"
    }
</script>

<style scoped>

</style>
