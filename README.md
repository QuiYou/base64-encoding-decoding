#pragma mark - base64 编码
- (NSString *)encode:(NSString *)string
{
    NSData *encodedata = [string dataUsingEncoding:NSUTF8StringEncoding];
    NSString *encodedStr = [encodedata base64EncodedStringWithOptions:0];
    return encodedStr;
}

/**
 * 使用方法
 * [self decodeString:@"5Y675L2g5aaI55qE"]
 */
#pragma mark - base64 解码
- (NSString *)decode:(NSString *)string
{
    NSData *decodedata = [[NSData alloc] initWithBase64EncodedString:string options:0];
    NSString *decodedStr = [[NSString alloc] initWithData:decodedata encoding:NSUTF8StringEncoding];
    return decodedStr;
}
